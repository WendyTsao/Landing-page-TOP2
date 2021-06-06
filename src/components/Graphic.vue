<template>
  <div class="col-12 col-lg-6" data-aos="fade-up" data-aos-mirror="true">
    <slot></slot>
    <img :src="require(`@/assets/pic/${image}`)" />
  </div>
</template>

<script>
export default {
  props: {
    image: {
      type: String,
    },
  },
};
</script>

<style>
</style>