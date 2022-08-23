<template>
  <header>
    <ul>
      <li v-for="(link, i) in headerLinks" :key="i">
        {{ link }}
      </li>
    </ul>
  </header>
</template>

<script>
export default {
  name: "BaseHeader",
  props: {
    headerLinks: Array,
  },
};
</script>

<style lang="scss" scoped></style>
