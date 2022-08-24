<template>
  <footer>
    <div class="container">
      <div class="row">
        <div class="col-6">
          <div class="text-white mb-3">{{ footerVoices[0].title }}</div>
          <ul>
            <li v-for="(voice, i) in footerVoices[0].voice" :key="i">
              {{ voice }}
            </li>
          </ul>
        </div>
        <div class="col-6">
          <div class="d-flex">
            <div class="w-50">
              <div class="text-white mb-3">{{ footerVoices[1].title }}</div>
              <ul class="d-flex flex-column flex-wrap flex-grow-1">
                <li v-for="(voice, i) in footerVoices[1].voice" :key="i">
                  {{ voice }}
                </li>
              </ul>
            </div>
            <div>
              <div class="text-white mb-3">{{ footerVoices[2].title }}</div>
              <ul>
                <li v-for="(voice, i) in footerVoices[2].voice" :key="i">
                  {{ voice }}
                </li>
              </ul>
            </div>
          </div>
        </div>
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
  background-color: #181621;

  padding: 50px 0;

  ul {
    padding: 0;
    max-height: 150px;
    li {
      color: grey;
      margin: 5px 0;
    }
  }
}
</style>
