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
            </div>
            <!-- Image -->
            <div class="col-8">
              <figure class="m-0 position-relative ps-5 pe-5">
                <img :src="allInfo.image" alt="photo" />
                <img :src="allInfo.imgYoutube" class="youtube-logo" v-if="allInfo.section === 'how-we-work'" />
              </figure>
            </div>
          </div>
        </div>
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
    display: flex;
    flex-direction: column;
    justify-content: center;
  }

  // Diamo un'altezza fissa alle figure di fianco alle descrizioni
  figure {
    height: 400px;

    .youtube-logo {
      position: absolute;
      top: 50%;
      left: 50%;
      transform: translate(-50%, -50%);

      width: 80px;
      height: 50px;
    }
  }
}
</style>
