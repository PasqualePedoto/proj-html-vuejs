<template>
  <div>
    <BaseHeader :headerLinks="headerLinks" class="header-position" />
    <BaseJumbotron :info="jumboInformations" />
    <BaseMain :blogs-card="blogsCard" :first-info="firstSectionsInfo" :second-info="secondSectionsInfo" :lessons-data="lessonsData" :grafic="graficImage" :courses="coursesData" />
    <BaseFooter :footer-voices="footerVoices" />
  </div>
</template>

<script>
import BaseHeader from "./components/BaseHeader.vue";
import BaseJumbotron from "./components/BaseJumbotron.vue";
import BaseMain from "./components/BaseMain.vue";
import BaseFooter from "./components/BaseFooter.vue";

export default {
  name: "App",
  components: {
    BaseHeader,
    BaseJumbotron,
    BaseMain,
    BaseFooter,
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

      // Primo insieme di sezioni che andranno prima del componente
      // contenente le card dei corsi
      firstSectionsInfo: [
        {
          section: "everithing-max-coach",
          female: `${require("./assets/images/about-us-01-ohkia3qg98rq9vg3s0mn2hkflr1migdqdw370qnegc.jpg")}`,
          image: `${require("./assets/images/stock-full-hd-10-ohki1ayywq3cqutettrncduujpoaorifqu4relt2ts.jpg")}`,
          imgYoutube: `${require("./assets/images/icon-youtube-play.png")}`,
          subtitle: "EVERYTHING IN MAXCOACH",
          title: [
            {
              text: "Learn about our ",
              color: "black",
            },
            {
              text: "Work Culture",
              color: "primary-color",
            },
            {
              text: " at MaxCoach",
              color: "black",
            },
          ],
          link: {
            type: "link",
            text: "Get Free Guide",
            desc: "Have questions?",
            color: "bg color",
          },
          paragraph:
            "Spend some time to visit our website or head office and discover our current courses,enrollment procedure,and registration deadline. We're opening new classes every beginning of each month",
        },
        {
          section: "how-we-work",
          image: `${require("./assets/images/stock-full-hd-11-670x450.jpg")}`,
          imgYoutube: `${require("./assets/images/icon-youtube-play.png")}`,
          subtitle: "HOW WE WORK",
          title: [
            {
              text: "Upgrade Your Skills ",
              color: "black",
            },
            {
              text: "Upgrade Your Life",
              color: "primary-color",
            },
          ],
          link: {
            type: "link",
            text: "Download free guidebook",
            desc: "",
            color: "bg black",
          },
          paragraph:
            "Spend some time to visit our website or head office and discover our current courses,enrollment procedure,and registration deadline. We're opening new classes every beginning of each month",
        },
      ],

      // Secondo insieme di sezioni che andranno dopo il componente
      // contenente le card dei corsi
      secondSectionsInfo: [
        {
          section: "testimonials",
          image: `${require("./assets/images/artist-blog-01-480x325.jpg")}`,
          imgYoutube: `${require("./assets/images/icon-youtube-play.png")}`,
          subtitle: "TESTIMONIALS",
          title: [
            {
              text: "Why Do Peaple ",
              color: "black",
            },
            {
              text: "*Hearts*",
              color: "primary-color",
            },
            {
              text: " Us?",
              color: "black",
            },
          ],
          link: {
            type: "link",
            text: "View all",
            desc: "",
            color: "bg black",
          },
          paragraph:
            "Spend some time to visit our website or head office and discover our current courses,enrollment procedure,and registration deadline. We're opening new classes every beginning of each month",
        },
        {
          section: "free-guide",
          image: `${require("./assets/images/home-3-team-image.png")}`,
          imgYoutube: `${require("./assets/images/icon-youtube-play.png")}`,
          subtitle: "EVERYTHING IN MAXCOACH",
          title: [
            {
              text: "We're Here To ",
              color: "black",
            },
            {
              text: "Transform",
              color: "primary-color",
            },
            {
              text: " You!",
              color: "black",
            },
          ],
          link: {
            type: "button",
            text: "Get Free Guide",
            desc: "",
            color: "color bg",
          },
          paragraph:
            "Spend some time to visit our website or head office and discover our current courses,enrollment procedure,and registration deadline. We're opening new classes every beginning of each month",
        },
      ],

      // Dati delle lezioni
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

      // Dati dei corsi
      coursesData: [
        {
          type: "course",
          src: `${require("./assets/images/course-02-480x298.jpg")}`,
          description: "Learning to Write as a Professional Author",
          cost: {
            int: "$40",
            dec: "00",
          },
          numberLessons: 20,
          numberStudents: 50,
        },
        {
          type: "course",
          src: `${require("./assets/images/stock-full-hd-03-480x298.jpg")}`,
          description: "Costumer-centric Info-Tech Strategies",
          cost: {
            int: "$00",
            dec: "00",
          },
          numberLessons: 24,
          numberStudents: 769,
        },
        {
          type: "course",
          src: `${require("./assets/images/stock-full-hd-04-480x298.jpg")}`,
          description: "Open Programming Courses for Everyone:Python",
          cost: {
            int: "$19",
            dec: "00",
          },
          numberLessons: 17,
          numberStudents: 62,
        },
      ],

      // Immagini di grafica
      graficImage: [
        {
          image: "maxcoach-shape-01",
          src: `${require("./assets/images/maxcoach-shape-01.png")}`,
        },
        {
          image: "maxcoach-shape-02",
          src: `${require("./assets/images/maxcoach-shape-02.png")}`,
        },
        {
          image: "maxcoach-shape-05",
          src: `${require("./assets/images/maxcoach-shape-05-100x100.png")}`,
        },
        {
          image: "maxcoach-shape-07",
          src: `${require("./assets/images/maxcoach-shape-07.png")}`,
        },
        {
          image: "svg-0",
          src: `${require("./assets/svg/svg-0.svg")}`,
        },
        {
          image: "mina-hollace",
          src: `${require("./assets/images/testimonial-avata-02.jpg")}`,
        },
        {
          image: "boy",
          src: `${require("./assets/images/testimonial-avata-01.jpg")}`,
        },
      ],

      // Dati per le cards dei Blogs
      blogsCard: [
        {
          type: "blog",
          src: `${require("./assets/images/artist-blog-03-480x325.jpeg")}`,
          subtitle: "ARTIST",
          description: "Brush Strokes Energize Trees in Paintings",
          date: "May 15,2020",
          views: 688,
        },
        {
          type: "blog",
          src: `${require("./assets/images/artist-blog-01-480x325.jpg")}`,
          subtitle: "ARTIST",
          description: "Pocket-Sized Notebooks Hold Miniature Paintings",
          date: "May 15,2020",
          views: 603,
        },
        {
          type: "blog",
          src: `${require("./assets/images/artist-blog-02-480x325.jpg")}`,
          subtitle: "ARTIST",
          description: "Connection Between Self-Portraits and Identity",
          date: "May 15,2020",
          views: 397,
        },
      ],

      // Voci del Footer
      footerVoices: [
        {
          title: "Address",
          voice: ["382 NE 191st # 87394 Miami, FI 33179-3899", "+1(305)547-9909(9am - 5pm EST,Monday - Friday)", "support@maxcoach.com"],
        },
        {
          title: "Explore",
          voice: ["Start here", "Blog", "About us", "Success story", "Courses", "Contact us"],
        },
        {
          title: "Information",
          voice: ["Merchandizing", "Purchase guide", "Privacy policy", "Terms of service"],
        },
      ],
    };
  },
  computed: {},
  methods: {},
};
</script>

<style lang="scss">
@import "./assets/scss/style.scss";

// Definisco le custom properties di cui avr?? bisogno
:root {
  --primary-color: #ef6f31;
  --secondary-color: #fff;
  --bgc-searchbar: #f5f5f5;
  --alternative-color: #2fab97;
  --bgc-main: #f7f7f7;
  --bgc-footer: #181621;
}

// Posizioniamo l'Header in modo tale da vederlo sempre
.header-position {
  position: sticky;
  top: 0;
  left: 0;
  right: 0;

  z-index: 10;

  box-shadow: 1px 2px 2px #dedede;
}
</style>
