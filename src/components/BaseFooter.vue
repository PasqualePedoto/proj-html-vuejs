<template>
  <footer class="position-relative">
    <div class="container">
      <div class="row">
        <!-- Sezione Sinistra del Footer -->
        <div class="col-6">
          <!-- ***** Prima Voce del Footer ***** -->
          <div class="text-white mb-3">{{ footerVoices[0].title }}</div>
          <!-- Lista di voci -->
          <ul>
            <li v-for="(voice, i) in footerVoices[0].voice" :key="i">
              <a href="#">{{ voice }}</a>
            </li>
          </ul>
        </div>
        <!-- Sezione destra del Footer -->
        <div class="col-6">
          <div class="d-flex">
            <div class="w-50">
              <!-- ***** Seconda Voce del Footer ***** -->
              <div class="text-white mb-3">{{ footerVoices[1].title }}</div>
              <!-- Lista di voci -->
              <ul class="d-flex flex-column flex-wrap flex-grow-1">
                <li v-for="(voice, i) in footerVoices[1].voice" :key="i">
                  <a href="#">{{ voice }}</a>
                </li>
              </ul>
            </div>
            <!-- ***** Terza Voce del Footer ***** -->
            <div>
              <div class="text-white mb-3">{{ footerVoices[2].title }}</div>
              <!-- Lista di voci -->
              <ul>
                <li v-for="(voice, i) in footerVoices[2].voice" :key="i">
                  <a href="#"> {{ voice }}</a>
                </li>
              </ul>
            </div>
          </div>
        </div>
        <!-- Set di Icon -->
        <div>
          <ul class="d-flex align-items-center">
            <li class="me-4">
              <a href="#"><i class="fa-brands fa-square-facebook fa-2x"></i></a>
            </li>
            <li class="me-4">
              <a href="#"><i class="fa-brands fa-twitter fa-2x"></i></a>
            </li>
            <li class="me-4">
              <a href="#"><i class="fa-brands fa-instagram fa-2x"></i></a>
            </li>
            <li class="me-4">
              <a href="#"><i class="fa-brands fa-linkedin fa-2x"></i></a>
            </li>
          </ul>
        </div>
        <!-- Scritta riguardante il copyright -->
        <div class="col-12 text-center copyright mt-5"><i class="fa-solid fa-copyright me-2"></i>2020 Maxcoach. All Rights Reserved</div>
        <!-- Freccetta verso l'alto -->
        <a href="#">
          <div class="up-arrow"><i class="fa-solid fa-arrow-up"></i></div>
        </a>
      </div>
    </div>
  </footer>
</template>

<script>
export default {
  name: "BaseFooter",
  props: {
    footerVoices: Array,
  },
};
</script>

<style lang="scss" scoped>
footer {
  // Freccetta in position absolute
  .up-arrow {
    width: 40px;
    height: 40px;

    border-radius: 50%;

    background-color: var(--primary-color);
    color: black;

    display: flex;
    align-items: center;
    justify-content: center;

    position: absolute;
    bottom: 10%;
    right: 10%;
  }
  // Definiamo il bg del Footer
  background-color: var(--bgc-footer);

  // Diamo un po d'aria
  padding: 50px 0;

  ul {
    // Settiamo il padding dell'ul
    padding: 0;

    // Altezza fissa così da creare l'effetto richiesto delle voci della
    // seconda lista di voci
    max-height: 120px;

    li {
      margin: 5px 0;
      a {
        // Definiamo i colori degli li
        color: grey;
        font-size: 12px;
      }
    }
  }

  // Definiamo il colore della scritta riguarda il copyright
  .copyright {
    color: grey;
    margin: 5px 0;
    font-size: 12px;
  }

  // Effetto di hover sui link del Footer
  li:hover a {
    color: white;
  }
}
</style>
