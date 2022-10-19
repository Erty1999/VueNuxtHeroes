<template>
  <div>
    <h3>{{ heroName }} Details</h3>
    <p>id: {{ heroId }}</p>
    <label>
      Hero name:
      <input type="text" :placeholder="heroName" />
    </label>
    <br />
    <br />
    <button>Back</button>
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
div {
  width: fit-content;
  font-size: 4vh;
  text-align: left;
  background-color: lightgrey;
  margin: 2vh 0 2vh 0;
  padding: 1vh 2vh 2vh 2vh;
  border-style: solid;
  border-color: black;
  border-width: 2px;
  border-radius: 1vh;
}

input {
  font-size: 4vh;
  width: 60%;
  border-style: solid;
  border-color: black;
  border-width: 2px;
  border-radius: 1vh;
}

label {
  font-weight: bold;
}

button {
  margin: 0vh 2vh 2vh 2vh;
  color: white;
  background-color: black;
}

button:hover {
  background-color: rgb(79, 78, 78);
}

.title {
  font-size: 8vh;
  color: darkblue;
}
</style>
