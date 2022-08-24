<template>
  <div>
    <a href="#"
      ><div class="link">{{ link }}<i class="ms-2 fa-solid fa-arrow-right"></i></div
    ></a>
  </div>
</template>

<script>
export default {
  name: "SectionLink",
  props: {
    link: String,
  },
};
</script>

<style lang="scss" scoped>
.link {
  // Cambiamo il display in modo tale da by-passare
  // lo stretch dei flex items
  display: inline-block;

  // Colore del testo
  color: #2fab97;

  // Box shadow
  box-shadow: 1px 2px 2px #dedede;

  padding: 0 2px;

  // Transitions sui colori
  transition: background-color 0.2s linear, color 0.2s linear;
}

// Effetto di hover sui links
a:hover .link {
  background-color: #2fab97;
  color: white;
}
</style>
