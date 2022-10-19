<template>
  <div class="hero-list">
    <h2>My Heroes</h2>
    <div class="hero-list-list">
      <HeroButton
        v-for="hero in heroList"
        :key="hero.id"
        :heroId="hero.id"
        :heroName="hero.heroName"
      />
    </div>
  </div>
</template>

<script>
import HeroButton from './heroButton.vue'
export default {
  props: {
    heroList: { type: Array, default: () => [] },
  },
  components: { HeroButton },
}
</script>

<style scoped>
.hero-list {
  border-top: 2px solid darkblue;
  margin-top: 3rem;
  display: flex;
  flex-direction: column;
}
.hero-list-list {
  display: flex;
  flex-direction: row;
  flex-wrap: wrap;
  gap: 2ch;
  margin: 0 auto;
}

.hero-list-list > * {
  min-width: 12ch;
}
</style>
