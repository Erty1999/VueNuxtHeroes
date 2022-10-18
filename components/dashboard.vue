<template>
  <div class="block_dashboard">
    <h2>Top Heroes</h2>
    <div class="dash_buttons">
      <button class="btn_topHero">Bombasto</button>
      <button class="btn_topHero">Celeritas</button>
      <button class="btn_topHero">Magneta</button>
      <button class="btn_topHero">RubberMan</button>
    </div>
  </div>
</template>

<script>
export default {
  props: {
    heroList: { type: Array, default: () => [] },
  },
}
</script>

<style scoped>
.block_dashboard {
  display: flex;
  flex-direction: column;
  width: fit-content;
  align-items: center;
  margin: auto;
  margin-bottom: 2rem;
}

.dash_buttons {
  display: flex;
  flex-direction: row;
}

.btn_topHero {
  color: white;
  background-color: black;
}

.btn_topHero:hover {
  background-color: rgb(79, 78, 78);
}

.btn_topHero:active {
  background-color: white;
  color: black;
}
</style>
