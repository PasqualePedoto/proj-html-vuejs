<template>
  <div>
    <BaseHeader :headerLinks="headerLinks" />
    <BaseJumbotron :info="jumboInformations" />
    <BaseMain :main-info="sectionsInfo" :lessons-data="lessonsData" />
  </div>
</template>

<script>
import BaseHeader from "./components/BaseHeader.vue";
import BaseJumbotron from "./components/BaseJumbotron.vue";
import BaseMain from "./components/BaseMain.vue";

export default {
  name: "App",
  components: {
    BaseHeader,
    BaseJumbotron,
    BaseMain,
  },
  data() {
    return {
      // Links nell'header
      headerLinks: ["Home", "Pages", "Courses", "Features", "Blog", "Shop"],

      // Oggetto contenente le info del jumbotron
      jumboInformations: {
        subtitle: "Commance Business",
        title: "Distant Mentoring Program",
        buttonText: "Download free guidebook",
      },

      sectionsInfo: [
        {
          section: "everithing-max-coach",
          image: `${require("./assets/images/stock-full-hd-10-ohki1ayywq3cqutettrncduujpoaorifqu4relt2ts.jpg")}`,
          subtitle: "EVERYTHING IN MAXCOACH",
          title: "Learn about our Work Culture at MaxCoach",
          paragraph:
            "Spend some time to visit our website or head office and discover our current courses,enrollment procedure,and registration deadline. We're opening new classes every beginning of each month",
        },
        {
          section: "how-we-work",
          image: `${require("./assets/images/stock-full-hd-11-670x450.jpg")}`,
          subtitle: "HOW WE WORK",
          title: "Upgrade Your Skills Upgrade Your Life",
          paragraph:
            "Spend some time to visit our website or head office and discover our current courses,enrollment procedure,and registration deadline. We're opening new classes every beginning of each month",
        },
        {
          section: "testimonials",
          image: `${require("./assets/images/rtl-demo-preview.jpg")}`,
          subtitle: "TESTIMONIALS",
          title: "Why Do Peaple *Hearts* Us?",
          paragraph:
            "Spend some time to visit our website or head office and discover our current courses,enrollment procedure,and registration deadline. We're opening new classes every beginning of each month",
        },
        {
          section: "free-guide",
          image: `${require("./assets/images/home-3-team-image-300x278.png")}`,
          subtitle: "EVERYTHING IN MAXCOACH",
          title: "We're Here To Transform You!",
          paragraph:
            "Spend some time to visit our website or head office and discover our current courses,enrollment procedure,and registration deadline. We're opening new classes every beginning of each month",
        },
      ],

      lessonsData: [
        {
          data: "129+",
          description: "ENROLLED LEARNERS",
        },
        {
          data: "80",
          description: "FINISHED SESSIONS",
        },
        {
          data: "4%",
          description: "SATISFACTION RATE",
        },
      ],

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
