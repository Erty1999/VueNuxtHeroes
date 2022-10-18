<template>
  <div class="details_block">
    <h2>{{ heroName }} Details</h2>
    <h3 class="id_style">id: {{ heroId }}</h3>
    <label class="hero_label">
      Hero name:
      <input class="hero_input" type="text" :placeholder="heroName" />
    </label>
    <br />
    <br />
    <button class="back_btn">Back</button>
  </div>
</template>

<script>
export default {
  data() {
    return {
      heroName: 'Magneta',
      heroId: '15',
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
  margin-left:1ch;
}

.hero_label {
  display: flex;
  font-weight: bold;
  margin-bottom: 2rem;
}

.back_btn {
  color: white;
  background-color: black;
}

.back_btn:hover {
  background-color: rgb(79, 78, 78);
}

.back_btn:active {
  background-color: white;
  color: black;
}
</style>
