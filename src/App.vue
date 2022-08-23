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

      // Palette dei colori
      white: "#ffffff",
      cinder: "#171520",
      delta: "#b1b1b0",
      texasRose: "#febc4d",
      stormDust: "#6c6c6b",
      mountainMeadow: "#1fad95",
      hawaiianTan: "#9f5d13",
      atlantis: "#94ca2b",
      catalinaBlue: "#08427d",
      shark: "#22272d",
      quillGray: "#e2e2e0",
      spicyMix: "#825c3f",
      gunsmoke: "#8a9391",
      driftwood: "#b08d52",
      pottersClay: "#7f5838",
      jungleGreen: "#2fab97",
      vulcan: "#141423",
      casablanca: "#f8b54e",
      lemonGrass: "#8c8d8a",
    };
  },
  computed: {},
  methods: {},
};
</script>

<style lang="scss">
@import "./assets/scss/style.scss";
</style>
