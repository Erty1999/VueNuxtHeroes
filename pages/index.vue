<template>
  <div class="card">
    <topPage />
  </div>
</template>

<script>
export default {
  data() {
    return {
      email: '',
    }
  },

  methods: {},
}
</script>

<style>
div {
  text-align: center;
  font-family: Impact, Haettenschweiler, 'Arial Narrow Bold', sans-serif;
}

button {
  font-size: 4vh;
  padding: 3vh;
  border-radius: 1vh;
  transition-duration: 0.2s;
}

.card {
  width: fit-content;
  margin: 2vh 0 0 0;
  padding: 2vh;
  border-style: solid;
  border-color: darkblue;
  border-width: 2px;
  border-radius: 1vh;
}
</style>
