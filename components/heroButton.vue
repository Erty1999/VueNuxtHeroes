<template>
  <div class="hero_btn">
    <span class="id_btn"> {{ heroId || -1 }}</span>
    <button class="name_btn" v-on:click="change_view('detail', heroId)">
      {{ heroName || 'unnamed' }}
    </button>
  </div>
</template>

<script>
export default {
  props: {
    heroName: { required: true, type: String },
    heroId: { type: String },
    change_view: Function,
  },
}
</script>

<style scoped>
.hero_btn {
  display: flex;
  flex-direction: row;
  align-items: center;
  width: fit-content;
  margin: 0.6rem 1rem;
}

.id_btn {
  font-size: 1.8rem;
  background-color: black;
  color: white;
  padding: 1em;
  border-top-left-radius: var(--br);
  border-bottom-left-radius: var(--br);
  height: 100%;
  width: fit-content;
}

.name_btn {
  height: 100%;
  width: fit-content;
  border-top-left-radius: 0;
  border-bottom-left-radius: 0;
  border: 2px solid black;
}
</style>
