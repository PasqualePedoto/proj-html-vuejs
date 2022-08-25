<template>
  <main>
    <!-- First Area -->
    <div class="gray-bg">
      <!-- First sections -->
      <CourseInformationSection :grafic="grafic" v-for="(info, i) in firstInfo" :key="i" :section="info.section" :allInfo="info" :direction="i" :lessons-data="lessonsData" />
      <!-- Latest Online Courses -->
      <BaseCourses :courses="courses" />
    </div>
    <!-- Second area -->
    <CourseInformationSection :grafic="grafic" v-for="(info, i) in secondInfo" :key="i + 'r'" :section="info.section" :allInfo="info" :direction="i" :lessons-data="lessonsData" />
    <div class="gray-bg pb-5">
      <TheOurBlogs :blogs-card="blogsCard" />
    </div>
    <BaseNewsletter class="pt-5 h-100" :grafic="grafic" />
  </main>
</template>

<script>
import CourseInformationSection from "./CourseInformationSection.vue";
import BaseCourses from "./BaseCourses.vue";
import TheOurBlogs from "./TheOurBlogs.vue";
import BaseNewsletter from "./BaseNewsletter.vue";
export default {
  name: "BaseMain",
  components: { CourseInformationSection, BaseCourses, TheOurBlogs, BaseNewsletter },
  props: {
    firstInfo: Array,
    secondInfo: Array,
    lessonsData: Array,
    grafic: Array,
    courses: Array,
    blogsCard: Array,
  },
};
</script>

<style lang="scss" scoped>
.gray-bg {
  background-color: var(--bgc-main);

  padding-top: 50px;
}
</style>
