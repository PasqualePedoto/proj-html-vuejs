<template>
  <section id="jumbotron">
    <div class="jumbo">
      <div class="container">
        <div class="row">
          <div class="col"></div>
        </div>
      </div>
    </div>
  </section>
</template>

<script>
export default {
  name: "BaseJumbotron",
};
</script>

<style lang="scss" scoped>
.jumbo {
  background-image: url("../assets/images/home-3-hero-bg.jpg");
  background-position: center;
  background-size: cover;
  background-repeat: no-repeat;

  width: 100%;
  height: 700px;
}
</style>
