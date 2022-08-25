<template>
  <div class="text-center mb-5">
    <div>
      <!-- Title -->
      <div>
        <h1 class="d-inline-block me-2">Subscribe</h1>
        <h1 class="d-inline-block text-primary-color">Newsletter</h1>
      </div>
      <!-- Paragraph -->
      <div>Enter your email address to register to our newsletter subscription delivered on a regular basis!</div>
      <!-- Content -->
      <div class="mt-5 d-flex align-items-center justify-content-evenly">
        <!-- Circle -->
        <figure class="m-0 image h-100 d-flex align-items-center">
          <img :src="grafic[1].src" :alt="grafic[0].image" />
        </figure>
        <!-- Email form -->
        <div class="form d-flex align-items-center justify-content-center">
          <input type="email" placeholder="Enter your email" />
          <BaseButton text="Subscribe" section="newsletter" class="p-0" color="bg-primary-color secondary-color" />
        </div>
        <!-- Grafic -->
        <div>
          <figure class="m-0 position-relative image">
            <img :src="grafic[3].src" :alt="grafic[3].image" class="rotate-square" />
            <img :src="grafic[1].src" :alt="grafic[1].image" class="effect-newsletter" />
          </figure>
        </div>
      </div>
    </div>
  </div>
</template>

<script>
import BaseButton from "./BaseButton.vue";
export default {
  name: "BaseNewsletter",
  components: { BaseButton },
  props: {
    grafic: Array,
  },
};
</script>

<style lang="scss" scoped>
.text-primary-color {
  color: var(--primary-color);
}

.form {
  height: 50px;

  input {
    background-color: var(--bgc-main);
    border: 0;
    padding: 10px;
  }
}

// Modelliamo le immagini di grafica
.image {
  width: 70px;
  height: 70px;

  // Posizioniamo il cerchio all'interno del quadrato rotato per
  // ottenere l'effetto grafico richiesto
  .effect-newsletter {
    position: absolute;
    top: 30%;
    left: 20%;
  }

  // Ruotiamo il quadrato di 307 gradi
  .rotate-square {
    transform: rotate(307deg);
  }
}
</style>
