<template>
  <div class="banner">
    <div class="container">
      <div class="menubar">
        <div class="logo">
          <img src="../assets/pic/Logo.png" alt="Top Logo" />
        </div>
        <div class="languages">
          <a class="languageItem">簡</a>
          <a class="languageItem">繁</a>
          <a class="languageItem">EN</a>
          <a class="menubar-open">
            <i class="fas fa-bars"></i>
          </a>
        </div>
      </div>
    </div>
    <div class="side-menu">
      <a class="menubar-close">
        <i class="fas fa-times fa-3x"></i>
      </a>
      <ul class="nav-bar">
        <li><a href="#">關於我們</a></li>
        <li><a href="#">企業介紹</a></li>
        <li><a href="#">線下分店</a></li>
        <li><a href="#">APP程式</a></li>
        <li><a href="#">聯絡我們</a></li>
        <li>
          <a href="#"><i class="fab fa-facebook-f"></i></a>
          <a href="#"><i class="fab fa-weixin"></i></a>
          <a href="#"><i class="fab fa-instagram"></i></a>
        </li>
      </ul>
    </div>
  </div>

  <div class="brand">
    <div class="container col-10 col-lg-8">
      <div class="row">
        <div class="txt">
          <h2>核心品牌矩阵</h2>
          <p>
            TOP2擁有一隊經驗豐富的頂尖駐歐洲買手團隊直接入口一線奢侈服裝品牌如
            GUCCI、DIOR、BURBERRY
            等，所有產品均百份百從各個歐洲品牌直接進口香港。我們秉承品牌核心價值，每天為追求時裝潮流的客人提供最新最緊貼歐洲潮流的產品。
          </p>
        </div>
      </div>
      <div class="brand-card">
        <div class="row">
          <div class="card-content col-12 col-lg-3">
            <img src="../assets/pic/brand01.jpg" />
            <div class="brand-name">
              <h3>古驰</h3>
            </div>
          </div>
          <!-- <div class="card-content col-12 col-lg-3">
                        <img src="../assets/pic/brand02.jpg">
                        <div class="brand-name">
                            <h3>迪奥</h3>
                        </div>
                    </div>
                    <div class="card-content col-12 col-lg-3">
                        <img src="../assets/pic/brand03.jpg">
                        <div class="brand-name">
                            <h3>芬迪</h3>
                        </div>
                    </div>
                    <div class="card-content col-12 col-lg-3">
                        <img src="../assets/pic/brand04.jpg">
                        <div class="brand-name">
                            <h3>巴黎世家</h3>
                        </div>
                    </div>
                    <div class="card-content col-12 col-lg-3">
                        <img src="../assets/pic/brand05.jpg">
                        <div class="brand-name">
                            <h3>博柏利</h3>
                        </div>
                    </div>
                    <div class="card-content col-12 col-lg-3">
                        <img src="../assets/pic/brand06.jpg">
                        <div class="brand-name">
                            <h3>紀梵希</h3>
                        </div>
                    </div> -->
        </div>
      </div>
    </div>
  </div>

  <div class="about">
    <div class="container col-10 col-lg-8">
      <div class="row">
        <div class="txt">
          <h2>关于我们</h2>
          <p>
            TOP2拥有超过30年经营欧洲时装品牌批发的经验，成为欧洲奢侈品牌的领先市场。  客户遍布亚洲各地，包括香港、澳门、中国、台湾及日本等。
          </p>
        </div>
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
            <li>
              <i class="fas fa-map-marker-alt"></i
              >九龙尖沙咀广东道30号新港中心G07铺 
            </li>
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
          <ul class="nav nav-tabs" id="myTab" role="tablist">
            <li class="nav-item" role="presentation">
              <button class="nav-link active" id="wholesale-tab" data-bs-toggle="tab"
                data-bs-target="#wholesale" type="button" role="tab"
                aria-controls="wholesale" aria-selected="true" >
                批发
              </button>
            </li>
            <li class="nav-item" role="presentation">
              <button class="nav-link" id="retail-tab" data-bs-toggle="tab"
                data-bs-target="#retail" type="button" role="tab"
                aria-controls="retail" aria-selected="false" >
                零售
              </button>
            </li>
          </ul>
          <div class="txt tab-content" id="myTabContent">
            <p class="tab-pane fade show active" id="wholesale"
              role="tabpanel" aria-labelledby="wholesale-tab" >
              TOP2的顶尖时装买手高瞻远瞩，拥有前瞻性的眼光能准确分析来季时装的潮流趋势，致力为客人提供最优越最新的时装产品。再配合我们卓越的分销渠道，客户遍布亚洲各国，包括香港、澳门、中国、台湾及日本等地。
            </p>
            <p class="tab-pane fade" id="retail"
              role="tabpanel" aria-labelledby="retail-tab" >
              亨德爾說過一句富有哲理的話，慎慮無後患。這句話幾乎解讀出了問題的根本。零售改變了我的命運。我們普遍認為，若能理解透徹核心原理，對其就有了一定的了解程度。零售對我來說，已經成為了我生活的一部分。
            </p>
          </div>
          <div class="business-img">
            <div>
              <img src="../assets/pic//business01.jpg" />
            </div>
          <!-- <div>
            <img src="../assets/pic//business02.jpg">
          </div> -->
          </div>
        </div>
      </div>
    </div>
  </div>

  <div class="app-screen">
    <div class="container col-10 col-lg-8">
      <div class="row">
        <div class="col-12 col-lg-6">
          <div class="txt">
            <span class="tag">即將推出</span>
            <h2>APP程式</h2>
            <p>
              自家研发B2B奢侈品电商平台让服装人没有难做的服装生意。即将会上线，请敬请期待!
            </p>
          </div>
          <img src="../assets/pic/Iphone.png" alt="" />
        </div>
        <div class="col-12 col-lg-6">
          <div class="txt">
            <h2>微信小程序 </h2>
            <p>
              透过微信庞大的社交体系，小程序得到快速传播最优越最新的时装产品最到我们的专贵客户，客源更多元化。
            </p>
          </div>
          <img src="../assets/pic/Iphone2.png" alt="" />
        </div>
      </div>
    </div>
  </div>

  <div class="contact">
    <div class="container col-10">
      <div class="row">
        <div class="txt">
          <h2>联络我们</h2>
        </div>
      </div>
      <div class="row">
        <div class="contact-item">
          <div class="txt">
            <p>联络电邮</p>
            <p>enquiry@top-2.hk</p>
          </div>
          <div class="txt">
            <p>加入我们电邮</p>
            <p>hr@top-2.hk</p>
          </div>
          <div class="txt">
            <p>合作电邮</p>
            <p>enquiry@top-2.hk</p>
          </div>
        </div>
      </div>
    </div>
  </div>

  <div class="footer">
    <div class="container-fluid">
      <div class="footer-link">
        <div class="copyright txt">© 2021 TOP2有限公司版權所有</div>
        <div class="menu txt">
          <a href="#">關於我們</a>
          <a href="#">企業介紹</a>
          <a href="#">線下分店</a>
          <a href="#">APP程式</a>
          <a href="#">聯絡我們</a>
        </div>
        <div class="contact-icon txt">
          <a href="#"><i class="fab fa-facebook-f"></i></a>
          <a href="#"><i class="fab fa-instagram"></i></a>
          <a href="#"><i class="fab fa-weixin"></i></a>
        </div>
      </div>
    </div>
  </div>
</template>

<script>
// @ is an alias to /src
import HelloWorld from "@/components/HelloWorld.vue";

export default {
  name: "Home",
  components: {
    HelloWorld,
  },
};
</script>
