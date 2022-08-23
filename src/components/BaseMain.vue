<template>
  <main>
    <!-- All sections -->
    <CourseInformationSection v-for="(info, i) in mainInfo" :key="i" :section="info.section" :allInfo="info" :direction="i" :lessons-data="lessonsData" />
  </main>
</template>

<script>
import CourseInformationSection from "./CourseInformationSection.vue";
export default {
  name: "BaseMain",
  components: { CourseInformationSection },
  props: {
    mainInfo: Array,
    lessonsData: Array,
  },
};
</script>

<style lang="scss" scoped></style>
