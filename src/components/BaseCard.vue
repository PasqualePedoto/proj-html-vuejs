<template>
  <div class="card">
    <!-- Card Image -->
    <figure class="card-element image m-0">
      <img :src="item.src" :alt="item.description" />
    </figure>
    <!-- Card Description -->
    <div class="card-element">
      <div v-if="type === 'course'" class="cost">{{ item.cost }}</div>
      <div class="desc">{{ item.description }}</div>
      <!-- Elementi propri del corso -->
      <div v-if="type === 'course'" class="course-info d-flex align-items-center">
        <div class="me-3"><i class="fa-solid fa-file-lines me-2"></i>{{ item.numberLessons }} Lessons</div>
        <div><i class="fa-regular fa-circle-user me-2"></i>{{ item.numberStudents }} Students</div>
      </div>
    </div>
  </div>
</template>

<script>
export default {
  name: "BaseCard",
  props: {
    item: Object,
    type: String,
  },
};
</script>

<style lang="scss" scoped>
.card {
  // Diamo un po d'aria
  margin: 10px;

  .card-element {
    height: 200px;
    width: 300px;

    text-align: start;

    // Diamo un po d'aria
    .desc,
    .cost,
    .course-info {
      padding: 10px;
      font-weight: bold;
    }

    // Cambiamo il colore del costo
    .cost {
      color: #2fab97;
    }
  }
}
</style>
