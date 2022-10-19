<template>
  <main>
    <div class="center card">
      <!-- <topPage />
      <heroList :heroList="Heroes" /> -->
      <!-- <Dashboard /> -->
      <HeroDetails />
    </div>
  </main>
</template>

<script>
import '/static/style.css'
import uniqueId from 'lodash.uniqueid'
import Dashboard from '~/components/dashboard.vueMagneta Details'
import HeroDetails from '~/components/heroDetails.vue'

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
  components: { Dashboard, HeroDetails },
}
</script>

<style></style>
