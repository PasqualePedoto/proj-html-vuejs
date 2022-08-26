<template>
  <div>
    <!-- All Courses Card -->
    <div class="d-flex align-items-center justify-content-center">
      <BaseCard v-for="(item, i) in courses" :key="i" :item="item" />
    </div>
    <!-- Pallini che dovrebbero fungere da carosello ma non funzionanti -->
    <div class="d-flex align-items-center justify-content-center pb-5 pt-5">
      <button class="circle active me-3"></button>
      <button class="circle me-3"></button>
      <button class="circle me-3"></button>
      <button class="circle me-3"></button>
      <button class="circle me-3"></button>
    </div>
  </div>
</template>

<script>
import BaseCard from "./BaseCard.vue";
export default {
  name: "BaseAllCourses",
  components: { BaseCard },
  props: {
    courses: Array,
  },
  data() {
    return {
      activeCourse: 1,
    };
  },
};
</script>

<style lang="scss" scoped>
// Definiamo i cerchi che dovrebbero racchiudere
// la logica del carosello
.circle {
  border-radius: 50%;
  width: 15px;
  height: 15px;

  background-color: #dedede;

  cursor: pointer;
  border: 0;
}

// Cerchio attivo
.circle.active {
  background-color: black;
  width: 25px;
  height: 25px;
}
</style>
