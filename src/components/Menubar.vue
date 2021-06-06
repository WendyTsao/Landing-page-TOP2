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
          <a class="menubar-open" @click="openMenu">
            <i class="fas fa-bars"></i>
          </a>
        </div>
      </div>
    </div>
    <div :class="['side-menu', {'hidden-menu':!menubarStatus}]">
      <a class="menubar-close" @click="closeMenu">
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
</template>

<script>
import { onMounted, ref } from 'vue';
export default {
    setup(){

        const menubarStatus = ref(false);
        const openMenu = ()=> menubarStatus.value = !menubarStatus.value;
        const closeMenu = ()=> menubarStatus.value = !menubarStatus.value;

        onMounted(() => {
            document.addEventListener('scroll', ()=> menubarStatus.value = true );
        });


        return { menubarStatus, openMenu ,closeMenu};
    }
};
</script>

<style scoped>
  .show-menu{ 
    transform: translateX(0);
  }

  .hidden-menu{
    transform: translateX(100%);
  }

</style>