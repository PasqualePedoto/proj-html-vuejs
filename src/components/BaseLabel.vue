<template>
  <div class="label">{{ text }}</div>
</template>

<script>
export default {
  name: "BaseLabel",
  props: {
    text: String,
  },
};
</script>

<style lang="scss" scoped>
.label {
  background-color: #ee7455;
  color: white;

  height: 40px;

  padding: 10px 15px;

  display: flex;
  align-items: center;
  justify-content: center;

  position: absolute;
  top: 0;
  right: 0;
}
</style>
