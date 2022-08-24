<template>
  <section :id="section">
    <div class="container">
      <div class="row">
        <!-- Text -->
        <div class="col-12 padding-y">
          <div class="row">
            <div class="col-4 flex-shrink-0 info" :class="{ 'order-1': direction % 2 === 1 }">
              <!-- Subtitle -->
              <h6>{{ allInfo.subtitle }}</h6>
              <!-- Title -->
              <div>
                <h1 class="d-inline-block me-2" v-for="(words, i) in allInfo.title" :key="i" :class="words.color">{{ words.text }}</h1>
              </div>
              <!-- Paragraph -->
              <p>{{ allInfo.paragraph }}</p>
              <!-- Link -->
              <SectionLink :link="allInfo.link" />
            </div>
            <!-- Image -->
            <div class="col-8">
              <div class="m-0 position-relative ps-5 pe-5 image block-image">
                <!-- ******************* -->
                <!-- Immagine principale della sezione -->
                <!-- ******************* -->
                <figure>
                  <img :src="allInfo.image" alt="photo" :class="{ 'w-auto': allInfo.section === 'free-guide' }" />
                </figure>
                <!-- * Effetti grafici sull'immagine principale -->
                <!-- Circle -->
                <figure class="grafic-image blue-ring">
                  <img :src="grafic[1].src" :alt="grafic[1].image" />
                </figure>
                <!-- Square: In base al posizionamento del testo cambiamo il posizionamento della grafica -->
                <figure class="grafic-image left-square" :class="{ 'right-square': direction % 2 === 1 }">
                  <img :src="grafic[3].src" :alt="grafic[3].image" />
                </figure>
                <!-- Hexagon: In base al posizionamento del testo cambiamo il posizionamento della grafica -->
                <figure class="grafic-image right-hexagon" :class="{ 'left-hexagon': direction % 2 === 1 }">
                  <img :src="grafic[2].src" :alt="grafic[2].image" />
                </figure>
                <!-- Gray Cloud: In base alla sezione cambiamo il posizionamento della nuvoletta -->
                <figure class="grafic-image cloud gray-cloud" v-if="allInfo.section === 'how-we-work'">
                  <img :src="grafic[4].src" :alt="grafic[4].image" />
                </figure>
                <!-- Green Cloud: In base alla sezione cambiamo il posizionamento della nuvoletta -->
                <figure class="grafic-image cloud green-cloud" v-if="allInfo.section === 'free-guide'">
                  <img :src="grafic[4].src" :alt="grafic[4].image" />
                </figure>
                <!-- Logo di You-Tube visibile solo in una sezione -->
                <figure class="youtube-logo">
                  <img :src="allInfo.imgYoutube" v-if="allInfo.section === 'how-we-work'" />
                </figure>
                <!-- Immagine di una donna visibile solo in una sezione -->
                <figure class="girl">
                  <img :src="allInfo.female" alt="" v-if="allInfo.section === 'everithing-max-coach'" />
                </figure>
                <!-- Immagine grafica: 3 lineette -->
                <figure class="grafic-image linear" v-if="allInfo.section === 'free-guide'">
                  <img :src="grafic[0].src" :alt="grafic[0].image" />
                </figure>
              </div>
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
import SectionLink from "./SectionLink.vue";

export default {
  name: "CourseInformationSection",
  components: {
    BaseLessonData,
    SectionLink,
  },
  props: {
    section: String,
    allInfo: Object,
    direction: Number,
    lessonsData: Array,
    grafic: Array,
  },
};
</script>

<style lang="scss" scoped>
section {
  // Padding lungo l'asse y
  .padding-y {
    padding: 130px 0;
  }
  // Flexiamo l'area delle info in modo talòe da disporle centralmente
  // rispetto alla foto di fianco
  .info {
    // Utilizato flex per disporre al meglio i contenuti testuali
    display: flex;
    flex-direction: column;
    justify-content: center;

    // Modelliamo i colori
    .green {
      color: #2fab97;
    }

    .black {
      color: black;
    }
  }
  // Diamo un'altezza fissa alle figure di fianco alle descrizioni
  .block-image {
    height: 400px;

    // Facciamo in modo che il figure segua il suo contenitore in altezza
    figure {
      height: 100%;

      // Serve a far emergere l'immagine principale con lo z-index
      position: absolute;
      z-index: 2;
    }

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

    // ***************
    // GRAFICA
    // ***************

    .grafic-image {
      // Dimensione degli elementi di grafica
      width: 100px;
      height: 100px;

      position: absolute;
    }

    //***************** */
    // Modelliamo l'anello blu e verde
    //***************** */

    .grafic-image.blue-ring {
      z-index: 3;

      top: 90%;
      left: 70%;
    }

    .grafic-image.linear {
      width: 120px;
      height: 120px;

      top: 86%;
      right: 90%;
    }

    //***************** */
    // Modelliamo i quadrati di puntini
    //***************** */

    // QUADRATO DI SINISTRA
    .grafic-image.left-square {
      z-index: 0;

      top: 85%;
      left: 0;
    }

    // QUADRATO DI DESTRA
    .grafic-image.right-square {
      z-index: 0;

      top: 85%;
      left: 0;
    }

    //***************** */
    // Modelliamo gli esagoni di puntini
    //***************** */

    // ESAGONO DI DESTRA
    .grafic-image.right-hexagon {
      z-index: 0;

      left: 80%;
      bottom: 90%;
    }

    // ESAGONO DI SINISTRA
    .grafic-image.left-hexagon {
      z-index: 0;

      top: 15%;
      left: 15%;
    }

    //***************** */
    // Modelliamo le nuvolette
    //***************** */

    .grafic-image.cloud {
      z-index: 0;

      bottom: 83%;
      right: 87%;
    }

    .grafic-image.cloud.gray-cloud {
      filter: opacity(0.1);
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

  // Modelliamo l'effetto di hover sul logo di youtube
  .image:hover {
    cursor: pointer;

    .youtube-logo {
      filter: contrast(200%);
    }
  }
}
</style>
