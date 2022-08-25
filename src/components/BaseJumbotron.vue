<template>
  <section id="jumbotron">
    <div class="jumbo position-relative">
      <div class="container h-100">
        <div class="row h-100">
          <div class="col h-100">
            <!-- Center Content -->
            <div class="d-flex align-items-center justify-content-center h-100">
              <div class="mb-5 text-center">
                <!-- Sub-Title -->
                <h3 class="text-white">{{ info.subtitle }}</h3>
                <!-- Title -->
                <h1 class="text-white">{{ info.title }}</h1>
                <!-- Button -->
                <BaseButton :text="info.buttonText" color="bg-secondary-color primary-color" />
                <!-- Barra degli strumenti posta in position absolute -->
                <div id="settings" class="d-flex flex-column">
                  <i class="fa-solid fa-ruler-combined mb-2"></i>
                  <i class="fa-solid fa-earth-africa mb-2"></i>
                  <i class="fa-solid fa-book mb-2"></i>
                  <i class="fa-solid fa-cart-shopping mb-2"></i>
                </div>
              </div>
            </div>
          </div>
        </div>
      </div>
    </div>
  </section>
</template>

<script>
import BaseButton from "./BaseButton.vue";
export default {
  name: "BaseJumbotron",
  components: { BaseButton },
  props: {
    info: Object,
  },
};
</script>

<style lang="scss" scoped>
// Definiamo lo sfondo del Jumbotron settando correttamente
// le properties del bg
.jumbo {
  background-image: url("../assets/images/home-3-hero-bg.jpg");
  background-position: center;
  background-size: cover;
  background-repeat: no-repeat;

  // Diamo un altezza fissa in modo da mostrare lo sfondo
  width: 100%;
  height: 700px;

  // Posizioniamo a lato la barra degli strumenti
  // Rifiniamo il blocco
  #settings {
    background-color: var(--secondary-color);

    position: absolute;
    top: 20%;
    right: 0;

    padding: 5px;
  }
}
</style>
