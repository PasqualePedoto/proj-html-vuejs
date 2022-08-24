<template>
  <button :class="color">
    <div class="button-in">{{ text }} <i class="fa-solid fa-arrow-right ms-2" v-show="section !== 'newsletter'"></i></div>
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

.bg-green {
  background-color: #2fab97;
}

.green {
  color: #2fab97;
}

.bg-white {
  background-color: #fff;
}

.white {
  color: white;
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
</style>
