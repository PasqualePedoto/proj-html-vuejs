<template>
  <div class="container">
    <div class="row pt-5">
      <div class="col text-center">
        <!-- Subtitle -->
        <h6 class="pt-5">JOIN MAXCOACH AT BEST</h6>
        <!-- Title -->
        <div class="h1">
          Latest Online
          <div class="text-primary-color d-inline h1">Courses</div>
        </div>
        <!-- Content -->
        <BaseAllCourses :courses="courses" />
        <!-- Description -->
        <div class="w-50 d-inline-block mb-5">
          Control your personal preference settings to get notified about appropriate courses.
          <a href="#" class="link">
            <div class="d-inline-block fw-bold">View all courses <i class="fa-solid fa-arrow-right-long"></i></div>
          </a>
        </div>
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
// Settiamo il colore di alcune parole del titolo
.text-primary-color {
  color: var(--primary-color);
}

// Creiamo il box-shadow
.link {
  box-shadow: 1px 2px 2px #dedede;
}
</style>
