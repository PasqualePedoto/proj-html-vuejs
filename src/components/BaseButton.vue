<template>
  <button :class="color">
    <div class="button-in hover-btn-jumbo h-100">
      {{ text }}
      <!-- Icona della freccia visibile solo se non ci troviamo nella sezione Newsletter oppure Header  -->
      <i class="fa-solid fa-arrow-right ms-2" v-show="section !== 'newsletter' && section !== 'header'"></i>
      <!-- Icona della lente di ingrandimento mostrata solo se il componente BaseButton -->
      <!-- E' definito nell Header -->
      <i class="fa-solid fa-magnifying-glass" v-show="section === 'header'"></i>
    </div>
  </button>
</template>

<script>
export default {
  name: "BaseButton",
  props: {
    text: String,
    section: String,
    color: String,
  },
};
</script>

<style lang="scss" scoped>
// Modelliamo i colori del il button

// * Colore principale: BG E COLOR
.bg-primary-color {
  background-color: var(--primary-color);
}

.primary-color {
  color: var(--primary-color);
}

// * Colore alternativo: BG E COLOR
.bg-alternative-color {
  background-color: var(--alternative-color);
}

.alternative-color {
  color: var(--alternative-color);
}

// * Colore secondario: BG E COLOR
.bg-secondary-color {
  background-color: var(--secondary-color);
}

.secondary-color {
  color: var(--secondary-color);
}

// Modelliamo il button
button {
  // Spaziature
  border: 0;
  // Dimensione del font
  font-size: 12px;
  font-weight: bold;

  // Ho dovuto forzare l'altezza
  height: 44px;

  .button-in {
    padding: 12px;
  }
}

// Effetto di Hover sul Button
button:hover .hover-btn-jumbo {
  background-color: var(--primary-color);
  color: var(--secondary-color);
}
</style>
