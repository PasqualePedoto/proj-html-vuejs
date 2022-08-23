<template>
  <form role="search">
    <div class="d-flex align-items-center justify-content-center">
      <input class="form-control me-2" type="search" :placeholder="placeholder" aria-label="Search" />
      <button class="btn btn-outline-success" type="submit">
        <a href="#"><i class="fa-solid fa-magnifying-glass"></i></a>
      </button>
    </div>
  </form>
</template>

<script>
export default {
  name: "BaseSearchbar",
  props: {
    placeholder: String,
  },
};
</script>

<style lang="scss" scoped>
form {
  // Settiamo la Searchbar eliminando le impostazioni
  // di BS
  div {
    background-color: #f5f5f5;

    input {
      border: 0;
      background-color: transparent;
    }
    button {
      border: 0;

      i {
        color: #58bcad;
      }
    }
  }
}
</style>
