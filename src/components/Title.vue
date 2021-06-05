<template>
  <div class="txt">
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