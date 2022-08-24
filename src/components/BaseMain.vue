<template>
  <main>
    <!-- All sections -->
    <CourseInformationSection :grafic="grafic" v-for="(info, i) in mainInfo" :key="i" :section="info.section" :allInfo="info" :direction="i" :lessons-data="lessonsData" />
    <!-- Latest Online Courses -->
    <BaseCourses :courses="courses" />
  </main>
</template>

<script>
import CourseInformationSection from "./CourseInformationSection.vue";
import BaseCourses from "./BaseCourses.vue";
export default {
  name: "BaseMain",
  components: { CourseInformationSection, BaseCourses },
  props: {
    mainInfo: Array,
    lessonsData: Array,
    grafic: Array,
    courses: Array,
  },
};
</script>

<style lang="scss" scoped></style>
