<template>
  <div class="btn">
    <span>{{ heroId || -1 }}</span>
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
.btn {
  display: flex;
  flex-direction: row;
  justify-content: left;
  align-items: center;
  font-size: 1.6rem;
}

span {
  display: inline-flex;
  justify-content: right;
  text-align: center;
  height: 100%;
  min-width: 3ch;
  padding: 0.6rem;
  background-color: black;
  color: white;
  border-radius: var(--br);
  border-bottom-right-radius: 0;
  border-top-right-radius: 0;
}

button {
  height: 100%;
  flex-grow: 1;
  border: 1px solid black;
  border-top-left-radius: 0;
  border-bottom-left-radius: 0;
}
</style>
