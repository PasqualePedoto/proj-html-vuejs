<template>
  <BaseHeader :headerLinks="headerLinks" />
</template>

<script>
import BaseHeader from "./components/BaseHeader.vue";
export default {
  name: "App",
  components: {
    BaseHeader,
  },
  data() {
    return {
      headerLinks: ["Home", "Pages", "Courses", "Features", "Blog", "Shop"],
    };
  },
  computed: {},
  methods: {},
};
</script>

<style lang="scss">
@import "./assets/scss/style.scss";
</style>
