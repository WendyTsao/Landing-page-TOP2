<template>
  <div class="col-12 col-lg-6">
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