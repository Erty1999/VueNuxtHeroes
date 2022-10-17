<template>
  <div>
    <h1>Top Heroes</h1>
    <button>Bombasto</button>
    <button>Celeritas</button>
    <button>Magneta</button>
    <button>RubberMan</button>
  </div>
</template>

<script>
export default {}
</script>

<style scoped>
div {
  width: fit-content;
  background-color: lightgrey;
  margin: 4vh 0 2vh 0;
  padding: 1vh 2vh 2vh 2vh;
  border-style: solid;
  border-color: black;
  border-width: 2px;
  border-radius: 1vh;
}

button {
  margin: 0vh 2vh 2vh 2vh;
  color: white;
  background-color: black;
  white-space: nowrap;
  overflow: hidden;
}

button:hover {
  background-color: rgb(79, 78, 78);
}
</style>
