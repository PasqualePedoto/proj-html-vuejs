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
// Settiamo l'etichetta
.label {
  // Colori e bg
  background-color: var(--primary-color);
  color: var(--secondary-color);

  height: 40px;

  padding: 10px 15px;

  // Centriamo la scritta dell'etichetta
  display: flex;
  align-items: center;
  justify-content: center;

  // Posizione assoluta così da inserirla
  // nell'angolo dell'immagine
  position: absolute;
  top: 0;
  right: 0;
}
</style>
