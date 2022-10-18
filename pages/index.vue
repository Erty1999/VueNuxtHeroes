<template>
  <main class="card">
    <topPage />
    <hr class="separation_row" />
    <heroList :heroList="Heroes" />
    <!--<dashboard :heroList="Heroes" />-->
    <!-- <hero-details/> -->
  </main>
</template>

<script>
import style from '@/static/style.css'
import lodash from 'lodash.uniqueid'
import uniqueId from 'lodash.uniqueid'
import dashboard from '~/components/dashboard.vue'
import TopPage from '~/components/topPage.vue'
import HeroList from '~/components/heroList.vue'
import HeroDetails from '~/components/heroDetails.vue'

export default {
  components: { dashboard, TopPage, HeroList, HeroDetails },
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

<style scoped>
.separation_row {
  padding: 0;
  margin: 2rem 0;
  width: 100%;
  color: darkblue;
}

.card {
  width: fit-content;
  padding: 0 2ch;
  border: 2px solid darkblue;
  border-radius: var(--br);
}
</style>
