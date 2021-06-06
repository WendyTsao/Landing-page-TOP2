<template>
  <Menubar></Menubar>

  <div class="brand">
    <div class="container col-10 col-lg-8">
      <div class="row">
        <Title :content="brandContents"></Title>
      </div>
      <Card></Card>
    </div>
  </div>

  <div class="about">
    <div class="container col-10 col-lg-8">
      <div class="row">
        <Title :content="aboutContents"></Title>
      </div>
    </div>
  </div>

  <div class="business">
      <div class="container col-10 col-lg-8">
          <div class="row">
              <div class="txt col-12 col-lg-4">
                  <h2>企业介绍</h2>
                  <ul>
                      <li>尖沙咀尖沙咀帝国店</li>
                      <li><i class="fas fa-map-marker-alt"></i>九龙尖沙咀广东道30号新港中心G07铺 </li>
                      <li><i class="far fa-clock"></i>星期一至星期日: 10:00 - 21:00 </li>
                      <li><i class="fas fa-phone-alt"></i>2130 7120</li>
                  </ul>
                  <!-- <ul>
                      <li>尖沙咀中心店</li>
                      <li><i class="fas fa-map-marker-alt"></i>香港九龙尖沙咀地道66 尖沙咀中心西翼 </li>
                      <li><i class="far fa-clock"></i>星期一至星期日: 10:00 - 21:00 </li>
                      <li><i class="fas fa-phone-alt"></i>2425 3425</li>
                  </ul> -->
              </div>
              <div class="content col-12 col-lg-8">
                  <ul class="nav nav-tabs" id="Tab" role="tablist">
                      <li class="nav-item" role="presentation">
                          <button class="nav-link active" id="wholesale-tab" data-bs-toggle="tab"
                              data-bs-target="#wholesale" type="button" role="tab" aria-controls="wholesale"
                              aria-selected="true">批发</button>
                      </li>
                      <li class="nav-item" role="presentation">
                          <button class="nav-link" id="retail-tab" data-bs-toggle="tab" data-bs-target="#retail"
                              type="button" role="tab" aria-controls="retail" aria-selected="false">零售</button>
                      </li>
                  </ul>
                  <div class="txt tab-content" id="TabContent">
                    <div class="tab-pane fade show active" id="wholesale" role="tabpanel" aria-labelledby="wholesale-tab">
                      <p>
                          TOP2的顶尖时装买手高瞻远瞩，拥有前瞻性的眼光能准确分析来季时装的潮流趋势，致力为客人提供最优越最新的时装产品。再配合我们卓越的分销渠道，客户遍布亚洲各国，包括香港、澳门、中国、台湾及日本等地。
                      </p>
                      <img src="../assets/pic/business01.jpg" />
                    </div>
                    <div class="tab-pane fade"  id="retail" role="tabpanel" aria-labelledby="retail-tab">
                      <p>
                          亨德爾說過一句富有哲理的話，慎慮無後患。這句話幾乎解讀出了問題的根本。零售改變了我的命運。我們普遍認為，若能理解透徹核心原理，對其就有了一定的了解程度。零售對我來說，已經成為了我生活的一部分。
                      </p>
                      <img src="../assets/pic/business02.jpg" />
                    </div>
                  </div>
              </div>
          </div>
      </div>
  </div>

  <div class="app-screen">
    <div class="container col-10 col-lg-8">
      <div class="row">
        <Graphic :image="'Iphone.png'">
          <Title :content="app1Contents">
            <span class="tag">即將推出</span>
          </Title>
        </Graphic>
        <Graphic :image="'Iphone2.png'" data-aos-delay="500">
          <Title :content="app2Contents"></Title>
        </Graphic>
      </div>
    </div>
  </div>

  <div class="contact">
    <div class="container col-10" data-aos="fade-up" data-aos-delay="500" data-aos-mirror="true">
      <div class="row">
        <Title :content="contactContents"></Title>
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
import Menubar from '../components/Menubar.vue';
import Card from '../components/Card.vue';
import Title from '../components/Title.vue';
import Graphic from '../components/Graphic.vue';

export default {
  components: {
    Menubar, Card, Title, Graphic,
  },

  setup(){
    const brandContents = 
    { title: "关于我们", 
      text: "TOP2擁有一隊經驗豐富的頂尖駐歐洲買手團隊直接入口一線奢侈服裝品牌如 GUCCI、DIOR、BURBERRY 等，所有產品均百份百從各個歐洲品牌直接進口香港。我們秉承品牌核心價值，每天為追求時裝潮流的客人提供最新最緊貼歐洲潮流的產品。" 
    };

    const aboutContents =
    { title: "核心品牌矩阵", 
      text: "TOP2拥有超过30年经营欧洲时装品牌批发的经验，成为欧洲奢侈品牌的领先市场。  客户遍布亚洲各地，包括香港、澳门、中国、台湾及日本等。" 
    };

    const app1Contents =
    { title: "APP程式", 
      text: "自家研发B2B奢侈品电商平台让服装人没有难做的服装生意。即将会上线，请敬请期待!" 
    };

    const app2Contents =
    { title: "微信小程序 ", 
      text: "透过微信庞大的社交体系，小程序得到快速传播最优越最新的时装产品最到我们的专贵客户，客源更多元化。" 
    };

    const contactContents =
    { title: "联络我们" };

    const contactItems = [
      { text:"联络电邮", email:"enquiry@top-2.hk" },
      { text:"加入我们电邮", email:"hr@top-2.hk" },
      { text:"合作电邮", email:"enquiry@top-2.hk" }
    ]

    return { brandContents, aboutContents, app1Contents, app2Contents, contactContents, contactItems }
  },
};
</script>
