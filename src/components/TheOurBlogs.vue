<template>
  <div class="text-center text-justify">
    <!-- Subtitle -->
    <div class="h6">READ FOR MORE JOYMENT</div>
    <!-- Title -->
    <div class="h1">
      <div class="d-inline-block me-2">Latest From</div>
      <div class="d-inline-block text-primary-color">Our Blogs</div>
    </div>
    <!-- Blogs cards -->
    <div class="d-flex align-content-center justify-content-center mt-5">
      <BaseCard v-for="(card, i) in blogsCard" :key="i" :item="card" />
    </div>
  </div>
</template>

<script>
import BaseCard from "./BaseCard.vue";
export default {
  name: "TheOurBlogs",
  components: { BaseCard },
  props: {
    blogsCard: Array,
  },
};
</script>

<style lang="scss" scoped>
.text-primary-color {
  color: var(--primary-color);
}
</style>
