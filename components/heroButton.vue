<template>
  <div>
    <span> {{ heroId || -1 }}</span>
    <button>{{ heroName || 'unnamed' }}</button>
  </div>
</template>

<script>
export default {
  props: {
    heroName: { required: true, type: String },
    heroId: { type: Number },
  },
}
</script>

<style scoped>
div {
  display: flex;
  flex-direction: row;
  margin: 1vh 0 1vh 0;
  justify-content: center;
  align-items: center;
  justify-content: center;
  align-items: center;
  border-radius: 1vh;
  width: fit-content;
  font-size: 4vh;
  background-color: black;
  color: white;
}

span {
  font-size: 4vh;
  margin-left: 3vh;
  margin-right: 2vh;
}

button {
  width: fit-content;
  border-top-left-radius: 0;
  border-bottom-left-radius: 0;
}
</style>
