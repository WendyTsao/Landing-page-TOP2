<template>
  <Menubar></Menubar>

  <div class="brand">
    <div class="container col-10 col-lg-8">
      <div class="row">
        <Title :content="contents.brand"></Title>
      </div>
      <Card></Card>
    </div>
  </div>

  <div class="about">
    <div class="container col-10 col-lg-8">
      <div class="row">
        <Title :content="contents.about"></Title>
      </div>
    </div>
  </div>

  <div class="business">
      <div class="container col-10 col-lg-8">
        <div class="row">
          <div class="txt col-12 col-lg-4" data-aos="fade-up" data-aos-duration="1000">
              <h2>企业介绍</h2>
              <transition name="fade">
                <ul v-show="isWholesale && retailDisable">
                    <li>尖沙咀尖沙咀帝国店</li>
                    <li><i class="fas fa-map-marker-alt"></i>九龙尖沙咀广东道30号新港中心G07铺 </li>
                    <li><i class="far fa-clock"></i>星期一至星期日: 10:00 - 21:00 </li>
                    <li><i class="fas fa-phone-alt"></i>2130 7120</li>
                </ul>
              </transition>
              <transition name="fade">
                <ul v-show="isRetail && wholesaleDisable">
                    <li>尖沙咀中心店</li>
                    <li><i class="fas fa-map-marker-alt"></i>香港九龙尖沙咀地道66 尖沙咀中心西翼 </li>
                    <li><i class="far fa-clock"></i>星期一至星期日: 10:00 - 21:00 </li>
                    <li><i class="fas fa-phone-alt"></i>2425 3425</li>
                </ul>
              </transition>
          </div>
          <div class="content col-12 col-lg-8">
            <ul class="nav nav-tabs" data-aos="fade-up" data-aos-duration="1000">
                <li><button @click="changeTab('批發')" :class="['nav-link',{'active': isWholesale}]">批发</button></li>
                <li><button @click="changeTab('零售')" :class="['nav-link',{'active': isRetail}]">零售</button></li>
            </ul>
            <div class="txt" data-aos="fade-left" data-aos-duration="1000">
              <transition name="fade">
                <div v-show="isWholesale && retailDisable">
                    <p>
                        TOP2的顶尖时装买手高瞻远瞩，拥有前瞻性的眼光能准确分析来季时装的潮流趋势，致力为客人提供最优越最新的时装产品。再配合我们卓越的分销渠道，客户遍布亚洲各国，包括香港、澳门、中国、台湾及日本等地。
                    </p>
                    <img src="../assets/pic/business01.jpg" />
                </div>
              </transition>
              <transition name="fade">
                <div v-show="isRetail && wholesaleDisable">
                    <p>
                        亨德爾說過一句富有哲理的話，慎慮無後患。這句話幾乎解讀出了問題的根本。零售改變了我的命運。我們普遍認為，若能理解透徹核心原理，對其就有了一定的了解程度。零售對我來說，已經成為了我生活的一部分。
                    </p>
                    <img src="../assets/pic/business02.jpg" />
                </div>
              </transition>
            </div>
          </div>
        </div>

      </div>
  </div>

  <div class="app-screen">
    <div class="container col-10 col-lg-8">
      <div class="row">
        <Graphic :image="'Iphone.png'">
          <Title :content="contents.app1">
            <span class="tag">即將推出</span>
          </Title>
        </Graphic>
        <Graphic :image="'Iphone2.png'" data-aos-delay="500">
          <Title :content="contents.app1"></Title>
        </Graphic>
      </div>
    </div>
  </div>

  <div class="contact">
    <div class="container col-10" data-aos="fade-up" data-aos-delay="200" data-aos-mirror="true">
      <div class="row">
        <Title :content="contents.contact"></Title>
      </div>
      <div class="row">
        <div class="contact-item">
          <div v-for="item in contactItems" class="txt" :key="item.email">
            <p>{{item.text}}</p>
            <p>{{item.email}}</p>
          </div>
        </div>
      </div>
    </div>
  </div>

</template>

<script>
// @ is an alias to /src
import { computed, ref } from 'vue';

import Menubar from '../components/Menubar.vue';
import Card from '../components/Card.vue';
import Title from '../components/Title.vue';
import Graphic from '../components/Graphic.vue';

export default {
  components: {
    Menubar, Card, Title, Graphic,
  },

  setup(){
    const contents = {
        brand: {
            title: "关于我们",
            text: "TOP2擁有一隊經驗豐富的頂尖駐歐洲買手團隊直接入口一線奢侈服裝品牌如 GUCCI、DIOR、BURBERRY 等，所有產品均百份百從各個歐洲品牌直接進口香港。我們秉承品牌核心價值，每天為追求時裝潮流的客人提供最新最緊貼歐洲潮流的產品。"
        },
        about: {
            title: "核心品牌矩阵",
            text: "TOP2拥有超过30年经营欧洲时装品牌批发的经验，成为欧洲奢侈品牌的领先市场。  客户遍布亚洲各地，包括香港、澳门、中国、台湾及日本等。"
        },
        app1: {
            title: "APP程式",
            text: "自家研发B2B奢侈品电商平台让服装人没有难做的服装生意。即将会上线，请敬请期待!"
        },
        app2: {
            title: "微信小程序",
            text: "透过微信庞大的社交体系，小程序得到快速传播最优越最新的时装产品最到我们的专贵客户，客源更多元化。"
        },
        contact: {
            title: "联络我们"
        }
    };

    const contactItems = [
      { text:"联络电邮", email:"enquiry@top-2.hk" },
      { text:"加入我们电邮", email:"hr@top-2.hk" },
      { text:"合作电邮", email:"enquiry@top-2.hk" }
    ]

    const currentTab = ref('批發');
    const wholesaleDisable = ref(false);
    const retailDisable = ref(true);

    const isRetail = computed(()=> currentTab.value === '零售');
    const isWholesale = computed(()=> currentTab.value === '批發');

    const changeTab = tabName => {
      currentTab.value = tabName;
      const time = setTimeout(() => {
        retailDisable.value = isWholesale.value;
        wholesaleDisable.value = isRetail.value;
      }, 1050);
    }

    return {
        contents,
        contactItems,
        isRetail,
        isWholesale,
        retailDisable,
        wholesaleDisable,
        changeTab
    };
  },
};
</script>
<style scoped>
    .fade-enter-active,
    .fade-leave-active {
        transition: opacity .5s;
    }

    .fade-enter-from,
    .fade-leave-to {
        opacity: 0;
    }

    .fade-enter-to,
    .fade-leave-from {
        opacity: 1;
    }
</style>