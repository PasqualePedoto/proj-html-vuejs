<template>
  <form role="search">
    <div class="d-flex align-items-center justify-content-center">
      <input class="form-control me-2" type="search" :placeholder="placeholder" aria-label="Search" />
      <BaseButton text="" color="primary-color bg-transparent" section="header" />
    </div>
  </form>
</template>

<script>
import BaseButton from "./BaseButton.vue";
export default {
  name: "BaseSearchbar",
  props: {
    placeholder: String,
  },
  components: { BaseButton },
};
</script>

<style lang="scss" scoped>
form {
  // Settiamo la Searchbar eliminando le impostazioni
  // di BS
  div {
    background-color: var(--bgc-searchbar);

    input {
      border: 0;
      background-color: transparent;
    }
    button {
      border: 0;

      i {
        color: var(--primary-color);
      }
    }

    // Modelliamo l'hover del Button modificando il BGC e il color
    button:hover {
      background-color: var(--primary-color);
    }

    button:hover a i {
      color: var(--secondary-color);
    }
  }
}
</style>
