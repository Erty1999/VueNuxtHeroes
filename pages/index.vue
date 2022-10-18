<template>
  <div class="card">
    <topPage />
    <heroList :heroList="Heroes"/> 
  </div>
</template>

<script>
import lodash from 'lodash.uniqueid'
import uniqueId from 'lodash.uniqueid'

export default {
  data() {
    return {
      Heroes: [
        { heroName: 'Dr. Nice', id: uniqueId() },
        { heroName: 'Bombasto', id: uniqueId() },
        { heroName: 'Celeritas', id: uniqueId() },
        { heroName: 'Magneta', id: uniqueId() },
        { heroName: 'RubberMan', id: uniqueId() },
        { heroName: 'Dynama', id: uniqueId() },
        { heroName: 'Dr. IQ', id: uniqueId() },
        { heroName: 'Magma', id: uniqueId() },
        { heroName: 'Tornado', id: uniqueId() },
      ],
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
