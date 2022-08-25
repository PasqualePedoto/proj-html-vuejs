<template>
  <div>
    <div v-if="link.type === 'button'">
      <button :class="link.color" class="info-button">{{ link.text }}</button>
    </div>
    <div v-else>
      <div v-if="link.desc !== ''" class="d-inline-block me-2">{{ link.desc }}</div>
      <a href="#" class="link">
        <div :class="link.color" class="d-inline-block">{{ link.text }}<i class="ms-2 fa-solid fa-arrow-right"></i></div
      ></a>
    </div>
  </div>
</template>

<script>
export default {
  name: "SectionLink",
  props: {
    link: Object,
  },
};
</script>

<style lang="scss" scoped>
// Settiamo lo stile del bottone
.info-button {
  padding: 10px;

  border: 0;
}

// Settiamo lo stile del link
.link {
  // Cambiamo il display in modo tale da by-passare
  // lo stretch dei flex items
  display: inline-block;

  // Box shadow
  box-shadow: 1px 2px 2px #dedede;

  padding: 0 2px;
}

//************* */
// COLORI DEI LINKS E BUTTONS
//************* */

button.bg {
  background-color: var(--primary-color);
}

.link .bg {
  background-color: var(--secondary-color);
}

button.color {
  color: var(--secondary-color);
}

.link .color {
  color: var(--primary-color);
}

.black {
  color: black;
}

.bg-black {
  background-color: black;
}
</style>
