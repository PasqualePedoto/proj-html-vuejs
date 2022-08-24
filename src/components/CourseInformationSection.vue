<template>
  <section :id="section" class="mt-5 mb-5">
    <div class="container">
      <div class="row">
        <!-- Text -->
        <div class="col-12">
          <div class="row">
            <div class="col-4 flex-shrink-0 info" :class="{ 'order-1': direction % 2 === 0 }">
              <!-- Subtitle -->
              <h6>{{ allInfo.subtitle }}</h6>
              <!-- Title -->
              <h1>{{ allInfo.title }}</h1>
              <!-- Paragraph -->
              <p>{{ allInfo.paragraph }}</p>
              <!-- Link -->
              <div>
                <a href="#"
                  ><div class="link">{{ allInfo.link }}<i class="ms-2 fa-solid fa-arrow-right"></i></div
                ></a>
              </div>
            </div>
            <!-- Image -->
            <div class="col-8">
              <figure class="m-0 position-relative ps-5 pe-5 image">
                <img :src="allInfo.image" alt="photo" />
                <img :src="allInfo.imgYoutube" class="youtube-logo" v-if="allInfo.section === 'how-we-work'" />
                <img :src="allInfo.female" alt="" class="girl" v-if="allInfo.section === 'everithing-max-coach'" />
              </figure>
            </div>
          </div>
        </div>
        <!-- Dati delle lezioni che verranno visualizzati solo in una sezione -->
        <div class="col-12 text-center d-flex align-items-center justify-content-center" v-if="allInfo.section === 'everithing-max-coach'">
          <BaseLessonData v-for="(info, i) in lessonsData" :key="i" class="data-lesson" :info="info" />
        </div>
      </div>
    </div>
  </section>
</template>
<script>
import BaseLessonData from "../components/BaseLessonData.vue";

export default {
  name: "CourseInformationSection",
  components: {
    BaseLessonData,
  },
  props: {
    section: String,
    allInfo: Object,
    direction: Number,
    lessonsData: Array,
  },
};
</script>

<style lang="scss" scoped>
section {
  // Flexiamo l'area delle info in modo talòe da disporle centralmente
  // rispetto alla foto di fianco
  .info {
    // Utilizato flex per disporre al meglio i contenuti testuali
    display: flex;
    flex-direction: column;
    justify-content: center;

    .link {
      // Cambiamo il display in modo tale da by-passare
      // lo stretch dei flex items
      display: inline-block;

      // Colore del testo
      color: #2fab97;

      // Box shadow
      box-shadow: 1px 2px 2px #dedede;

      padding: 0 2px;

      // Transitions sui colori
      transition: background-color 0.2s linear, color 0.2s linear;
    }

    // Effetto di hover sui links
    a:hover .link {
      background-color: #2fab97;
      color: white;
    }
  }

  // Diamo un'altezza fissa alle figure di fianco alle descrizioni
  figure {
    height: 400px;

    // Fissiamo il logo di youtube al centro dell'immagine ma solo della
    // sezione 'How we work'
    .youtube-logo {
      position: absolute;
      top: 50%;
      left: 50%;
      transform: translate(-50%, -50%);

      width: 80px;
      height: 50px;
    }

    // Fissiamo l'immagine della donna al centro dell'immagine ma solo della
    // sezione 'everything in maxcoach'
    .girl {
      position: absolute;
      left: 85%;
      bottom: 80%;

      width: 110px;
      height: 110px;
    }
  }
}

// Modelliamo l'effetto di hover sul logo di youtube
.image:hover {
  cursor: pointer;

  .youtube-logo {
    filter: contrast(200%);
  }
}
</style>
