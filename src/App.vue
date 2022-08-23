<template>
  <div>
    <BaseHeader :headerLinks="headerLinks" />
    <BaseJumbotron />
  </div>
</template>

<script>
import BaseHeader from "./components/BaseHeader.vue";
import BaseJumbotron from "./components/BaseJumbotron.vue";
export default {
  name: "App",
  components: {
    BaseHeader,
    BaseJumbotron,
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
