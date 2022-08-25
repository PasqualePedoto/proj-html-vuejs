<template>
  <div class="card">
    <!-- Card Image -->
    <figure class="card-element image m-0 position-relative">
      <img :src="item.src" :alt="item.description" />
      <!-- Label "FREE" -->
      <BaseLabel text="FREE" v-if="item.description === 'Costumer-centric Info-Tech Strategies' && type === 'course'" />
    </figure>
    <!-- Card Description -->
    <div class="card-element">
      <!-- Course Element -->
      <div v-if="type === 'course'" class="cost">
        <div class="d-inline-block">{{ item.cost.int }}</div>
        <div class="decimal d-inline-block">.{{ item.cost.dec }}</div>
      </div>
      <!-- Blogs Post Element -->
      <div v-if="type === 'blogs'" class="subtitle">
        <div>{{ item.subtitle }}</div>
      </div>
      <!-- Element Description -->
      <div class="desc">{{ item.description }}</div>
      <!-- Elementi propri del corso -->
      <div v-if="type === 'course'" class="course-info d-flex align-items-center">
        <div class="me-3"><i class="fa-solid fa-file-lines me-2"></i>{{ item.numberLessons }} Lessons</div>
        <div><i class="fa-regular fa-circle-user me-2"></i>{{ item.numberStudents }} Students</div>
      </div>
      <!-- Elementi propri del post sul Blog -->
      <div v-if="type === 'blogs'" class="d-flex align-items-center views-date">
        <div class="me-3"><i class="fa-solid fa-calendar-days me-2"></i>{{ item.date }}</div>
        <div><i class="fa-solid fa-eye me-2"></i>{{ item.views }}</div>
      </div>
    </div>
  </div>
</template>

<script>
import BaseLabel from "./BaseLabel.vue";
export default {
  name: "BaseCard",
  props: {
    item: Object,
    type: String,
  },
  components: { BaseLabel },
};
</script>

<style lang="scss" scoped>
.card {
  // Diamo un po d'aria
  margin: 10px;

  // Un po di ombreggiatura
  box-shadow: 4px 6px 6px #dedede;

  .card-element {
    height: 200px;
    width: 300px;

    text-align: start;

    // Rendiamo il numero decimale più piccolo
    .decimal {
      font-size: 10px;
    }

    // Diamo un po d'aria
    .desc,
    .cost,
    .course-info,
    .views-date,
    .subtitle {
      padding: 10px;
      font-weight: bold;
    }

    .subtitle,
    .views-date {
      color: gray;
      font-weight: normal;
      font-size: 12px;
    }

    // Cambiamo il colore del costo
    .cost {
      color: #2fab97;
    }
  }
}
</style>
