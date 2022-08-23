<template>
  <section id="jumbotron">
    <div class="jumbo">
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
                <BaseButton :text="info.buttonText" />
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
.jumbo {
  background-image: url("../assets/images/home-3-hero-bg.jpg");
  background-position: center;
  background-size: cover;
  background-repeat: no-repeat;

  width: 100%;
  height: 700px;
}
</style>
