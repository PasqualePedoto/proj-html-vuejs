<template>
  <div>
    <div class="d-flex align-items-center justify-content-center">
      <BaseCard v-for="(item, i) in courses" :key="i" :item="item" type="course" />
    </div>
    <div class="d-flex align-items-center justify-content-center mt-md-3">
      <button class="circle me-3" @click="changeCourse"></button>
      <button class="circle me-3" @click="changeCourse"></button>
      <button class="circle me-3" @click="changeCourse"></button>
      <button class="circle me-3" @click="changeCourse"></button>
      <button class="circle me-3" @click="changeCourse"></button>
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
  methods: {
    changeCourse() {},
  },
};
</script>

<style lang="scss" scoped>
.circle {
  border-radius: 50%;
  width: 15px;
  height: 15px;

  background-color: #dedede;

  cursor: pointer;
  border: 0;
}

.circle.active {
  background-color: black;
  width: 25px;
  height: 25px;
}
</style>
