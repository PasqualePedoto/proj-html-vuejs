<template>
  <div>
    <!-- Se è un Button -->
    <div v-if="link.type === 'button'">
      <BaseButton :class="link.color" :text="link.text" section="info" />
      <!-- <button :class="link.color" class="info-button">{{ link.text }}</button> -->
    </div>
    <!-- Se è un link -->
    <div v-else>
      <div v-if="link.desc !== ''" class="d-inline-block me-2">{{ link.desc }}</div>
      <a href="#" class="link p-0">
        <div :class="link.color" class="d-inline-block w-100">{{ link.text }}<i class="ms-2 fa-solid fa-arrow-right"></i></div
      ></a>
    </div>
  </div>
</template>

<script>
import BaseButton from "./BaseButton.vue";
export default {
  name: "SectionLink",
  props: {
    link: Object,
  },
  components: { BaseButton },
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

// Effetto di hover sui link
.link:hover div {
  background-color: var(--primary-color);
  color: var(--secondary-color);
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
