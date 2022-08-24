<template>
  <div class="container">
    <div class="row pt-5">
      <div class="col text-center">
        <!-- Subtitle -->
        <h6 class="pt-5">JOIN MAXCOACH AT BEST</h6>
        <!-- Title -->
        <div class="h1">
          Latest Online
          <div class="text-green d-inline h1">Courses</div>
        </div>
        <!-- Content -->
        <BaseAllCourses :courses="courses" />
      </div>
    </div>
  </div>
</template>

<script>
import BaseAllCourses from "./BaseAllCourses.vue";
export default {
  name: "BaseCourses",
  components: { BaseAllCourses },
  props: {
    courses: Array,
  },
};
</script>

<style lang="scss" scoped>
.text-green {
  color: #2fab97;
}
</style>
