<template>
  <div>
    <h1>Tour of Heroes</h1>
    <div class="block_btn">
      <button class="space" v-on:click="change_view('dash')">Dashboard</button>
      <button v-on:click="change_view('list')">Heroes</button>
    </div>
  </div>
</template>

<script>
export default {
  props: {
    change_view: Function,
  },
}
</script>

<style scoped>
.block_btn {
  display: flex;
  flex-direction: row;
  width: fit-content;
  margin: auto;
}

.space {
  margin-right: 2rem;
}
</style>
