<template>
  <button class="btn">{{ text }} <i class="fa-solid fa-arrow-right ms-2"></i></button>
</template>

<script>
export default {
  name: "BaseButton",
  props: {
    text: String,
  },
};
</script>

<style lang="scss" scoped>
// Modelliamo il button
button {
  background-color: white;
  color: #2fab97;

  padding: 12px;

  //   transition: background-color 0.025s linear, color 0.5s linear;
}

// Effetto di hover sul button
button:hover {
  background-color: #2fab97;
  color: white;
}
</style>
