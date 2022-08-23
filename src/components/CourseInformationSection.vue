<template>
  <section :id="section" class="mt-5 mb-5">
    <div class="container">
      <div class="row">
        <!-- Text -->
        <div class="col-12">
          <div class="row">
            <div class="col-4 flex-shrink-0" :class="{ 'order-1': direction % 2 === 0 }">
              <!-- Subtitle -->
              <h6>{{ allInfo.subtitle }}</h6>
              <!-- Title -->
              <h1>{{ allInfo.title }}</h1>
              <!-- Paragraph -->
              <p>{{ allInfo.paragraph }}</p>
            </div>
            <!-- Image -->
            <div class="col-8 cicc"></div>
          </div>
        </div>
        <div class="col-12" v-if="allInfo.section === 'everithing-max-coach'"></div>
      </div>
    </div>
  </section>
</template>

<script>
export default {
  name: "CourseInformationSection",
  props: {
    section: String,
    allInfo: Object,
    direction: String,
  },
};
</script>

<style lang="scss" scoped>
section {
  .cicc {
    background-color: red;
  }
}
</style>
