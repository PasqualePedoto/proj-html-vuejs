<template>
  <header>
    <div class="container">
      <div class="row">
        <div class="col">
          <!-- Header Content -->
          <div class="d-flex justify-content-between">
            <!-- Header links -->
            <div class="d-flex align-items-center justify-content-center">
              <ul class="d-flex align-items-center justify-content-center m-0">
                <li v-for="(link, i) in headerLinks" :key="i" class="me-3">
                  <div class="d-flex align-items-center justify-content-center">
                    <a href="#" class="me-1">{{ link }}<i class="ms-1 fa-solid fa-angle-down"></i></a>
                  </div>
                </li>
              </ul>
            </div>
            <!-- Header Logo -->
            <figure class="m-0 d-flex align-items-center align-self-center">
              <a href="#">
                <img src="../assets/images/dark-logo.png" alt="dark-logo" class="img-fluid" />
              </a>
            </figure>
            <!-- Header Searchbar -->
            <nav class="d-flex align-items-center justify-content-center">
              <a href="#"
                ><i class="fa-solid fa-cart-shopping me-3 position-relative">
                  <div class="cart d-flex align-items-center justify-content-center">0</div>
                </i></a
              >
              <a href="#"><i class="fa-regular fa-circle-user me-3"></i></a>
              <BaseSearchbar placeholder="Search..." />
            </nav>
          </div>
        </div>
      </div>
    </div>
  </header>
</template>

<script>
import BaseSearchbar from "./BaseSearchbar.vue";
export default {
  name: "BaseHeader",
  props: {
    headerLinks: Array,
  },
  components: { BaseSearchbar },
};
</script>

<style lang="scss" scoped>
header {
  background-color: var(--secondary-color);

  li:hover a {
    color: var(--primary-color);
  }

  figure {
    width: 130px;
    height: 100px;
  }

  // Posizioniamo il numero di elementi presenti nel carrello
  nav .cart {
    background-color: var(--primary-color);
    color: var(--secondary-color);

    width: 15px;
    height: 15px;

    border-radius: 50%;
    font-size: 10px;

    position: absolute;
    bottom: 90%;
    left: 90%;
  }
}
</style>
