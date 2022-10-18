<template>
  <div>
    <h1>My Heroes</h1>
    <heroButton
      v-for="hero in heroList"
      :key="hero.id"
      :heroId="hero.id"
      :heroName="hero.heroName"
    />
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
div {
  text-align: left;
  font-size: 2vh;
  margin-top: 2vh;
  display: flex;
  flex-direction: column;
}
</style>
