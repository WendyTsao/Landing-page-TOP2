<template>
  <div class="txt" data-aos="fade-up" data-aos-duration="1000" data-aos-mirror="true">
    <slot></slot>
    <h2>{{ content.title }}</h2>
    <p>{{ content.text }}</p>
  </div>
</template>

<script>
export default {
  props: {
    content: {
      type: Object,
    },
  },
};
</script>

<style>
</style>