<template>
  <div class="brand-card">
    <div class="row">
      <Swiper :slidesPerView="2" :spaceBetween="30" :slidesPerGroup="2"
              :grabCursor="true"  :scrollbar="true"  class="mySwiper" 
              :breakpoints="{ '992': { slidesPerView: 4, spaceBetween: 20, slidesPerGroup: 4 }}">
        <SwiperSlide v-for="brand in brands" class="card-content col-12 col-lg-3" :key="brand.image">
          <img :src="require(`@/assets/pic/${brand.image}`)" />
          <div class="brand-name">
            <h3>{{brand.name}}</h3>
          </div>
        </SwiperSlide>
      </Swiper>
    </div>
  </div>
</template>

<script>
import { Swiper, SwiperSlide } from 'swiper/vue';
import 'swiper/swiper.min.css';
import "swiper/components/scrollbar/scrollbar.min.css"

import SwiperCore, { Scrollbar } from "swiper/core";
SwiperCore.use([Scrollbar]);


export default {
    components: {
     Swiper, SwiperSlide,
  },

    setup(){
        const brands = [
            { image: "brand01.jpg", name: "古驰" },
            { image: "brand02.jpg", name: "迪奥" },
            { image: "brand03.jpg", name: "芬迪" },
            { image: "brand04.jpg", name: "巴黎世家" },
            { image: "brand05.jpg", name: "博柏利" },
            { image: "brand06.jpg", name: "紀梵希" }
        ];

        return { brands };
    }
};
</script>

<style>
</style>