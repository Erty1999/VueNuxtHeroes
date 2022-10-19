<template>
  <div class="details_block">
    <h2>{{ hero.heroName }} Details</h2>
    <h3 class="id_style">id: {{ hero.id }}</h3>
    <label class="hero_label">
      Hero name:
      <input v-model="new_name" class="hero_input" type="text" :placeholder="hero.heroName" />
    </label>
    <br />
    <br />
    <div class="block_btn"> 
      <button v-on:click="change_hero(change_hero(new_name,hero.id))">Change</button>
      <button v-on:click="back" class="back_btn">Back</button>
      
    </div>
  </div>
</template>

<script>
export default {
  props: {
    hero: Object,
    change_view: Function,
    back: Function,
    change_hero: Function,
  },
  data() {
    return {
      new_name: ""
    }
  },
}
</script>

<style scoped>
.details_block {
  display: flex;
  flex-direction: column;
  align-items: center;
  width: fit-content;
  font-size: 1.8rem;
  margin: auto;
  margin-bottom: 2rem;
}

.id_style {
  margin: 0 0 2rem 0;
}

.hero_input {
  font-size: 1.8rem;
  border-style: solid;
  border-color: black;
  border-width: 2px;
  border-radius: var(--br);
  padding-left: 1ch;
  margin-left: 1ch;
}

.hero_label {
  display: flex;
  font-weight: bold;
  margin-bottom: 2rem;
}

.block_btn{
  display:flex;
  flex-direction: row;
}

.back_btn {
  color: white;
  background-color: black;
  margin-left: 2rem;
}

.back_btn:hover {
  background-color: rgb(79, 78, 78);
}

.back_btn:active {
  background-color: white;
  color: black;
}
</style>
