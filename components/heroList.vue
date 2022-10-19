<template>
  <div class="block_heroes">
    <h2>My Heroes</h2>
    <div class="block_list">
      <heroButton
        v-for="hero in heroList"
        :key="hero.id"
        :heroId="hero.id"
        :heroName="hero.heroName"
        :change_view="change_view"
      />
    </div>
  </div>
</template>

<script>
import heroButton from './heroButton.vue'
export default {
  components: { heroButton },
  props: {
    heroList: { type: Array, default: () => [] },
    change_view: Function,
  },
}
</script>

<style scoped>
.block_heroes {
  display: flex;
  flex-direction: column;
  align-items: center;
}

.block_list {
  display: flex;
  flex-direction: row;
  flex-wrap: wrap;
  margin: 0 2rem 2rem 2rem;
}
</style>
