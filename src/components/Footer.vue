<template>
  <div class="footer">
    <div class="container-fluid">
      <div class="footer-link">
        <div class="copyright txt">&copy; 2021 TOP2有限公司版權所有</div>
        <div class="menu txt">
          <a v-for="menu in menuContents" :href="menu.link" :key="menu.link">{{menu.title}}</a>
        </div>
        <div class="contact-icon txt">
            <a v-for="contact in contactContents"  :href="contact.link" :key="contact.link">
                <i :class="contact.iconClass"></i>
            </a>
        </div>
      </div>
    </div>
  </div>
</template>

<script>
export default {
    setup(){
        const menuContents = [
            { link: "#", title: "關於我們" },
            { link: "#", title: "企業介紹" },
            { link: "#", title: "線下分店" },
            { link: "#", title: "關於我們" },
            { link: "#", title: "APP程式" }
        ];

        const contactContents = [
            { link: "#", iconClass: "fab fa-facebook-f" },
            { link: "#", iconClass: "fab fa-instagram" },
            { link: "#", iconClass: "fab fa-weixin" }
        ];

        return { menuContents, contactContents };
    },
};
</script>

<style>
</style>