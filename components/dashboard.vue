<template>
  <div class="block_dashboard">
    <h2>Top Heroes</h2>
    <div class="dash_buttons">
      <span 
      v-for="hero in heroList" 
      :key="hero.id" >
      <button 
      v-if="hero.id <=4"
      class="btn_topHero"
      v-on:click="change_view('detail', hero.id)">{{hero.heroName}}</button>
      </span>
    </div>
  </div>
</template>

<script>
export default {
  props: {
    heroList: { type: Array, default: () => [] },
    change_view: Function,
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
