<template>
  <div class="brand-card">
    <div class="row">
      <div v-for="brand in brands" class="card-content col-12 col-lg-3" :key="brand.image">
        <img :src="require(`@/assets/pic/${brand.image}`)" />
        <div class="brand-name">
          <h3>{{brand.name}}</h3>
        </div>
      </div>
    </div>
  </div>
</template>

<script>
export default {
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