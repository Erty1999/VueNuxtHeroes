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
  margin: 1rem 0;
  padding: 1rem;
  border-style: solid;
  border-color: black;
  border-width: 2px;
  border-radius: var(--br);
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
