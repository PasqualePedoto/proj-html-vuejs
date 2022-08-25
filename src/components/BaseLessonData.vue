<template>
  <div class="data-lesson">
    <p class="number">{{ info.data }}</p>
    <p class="desc">{{ info.description }}</p>
  </div>
</template>

<script>
export default {
  name: "BaseLessonData",
  props: {
    info: Object,
  },
};
</script>

<style lang="scss" scoped>
.data-lesson {
  width: 100px;
  margin: 40px;

  font-weight: bold;

  .number {
    font-size: 30px;
    color: var(--primary-color);
  }

  .desc {
    font-size: 12px;
  }
}
</style>
