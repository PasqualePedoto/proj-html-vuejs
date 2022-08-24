<template>
  <main>
    <!-- First Area -->
    <div id="top-area">
      <!-- First sections -->
      <CourseInformationSection :grafic="grafic" v-for="(info, i) in firstInfo" :key="i" :section="info.section" :allInfo="info" :direction="i" :lessons-data="lessonsData" />
      <!-- Latest Online Courses -->
      <BaseCourses :courses="courses" />
    </div>
    <!-- Second area -->
    <CourseInformationSection :grafic="grafic" v-for="(info, i) in secondInfo" :key="i + 'r'" :section="info.section" :allInfo="info" :direction="i" :lessons-data="lessonsData" />
  </main>
</template>

<script>
import CourseInformationSection from "./CourseInformationSection.vue";
import BaseCourses from "./BaseCourses.vue";
export default {
  name: "BaseMain",
  components: { CourseInformationSection, BaseCourses },
  props: {
    firstInfo: Array,
    secondInfo: Array,
    lessonsData: Array,
    grafic: Array,
    courses: Array,
  },
};
</script>

<style lang="scss" scoped>
#top-area {
  background-color: #f7f7f7;
}
</style>
