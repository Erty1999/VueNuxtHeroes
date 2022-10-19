<template>
  <main class="card">
    <topPage :change_view="show_component" />
    <hr class="separation_row" />
    <heroList
      :heroList="Heroes"
      :change_view="show_component"
      v-if="active_component === 'list'"
    />
    <dashboard
      :heroList="Heroes"
      :change_view="show_component"
      v-if="active_component === 'dash'"
    />
    <hero-details
      :hero="hero_details"
      :back="back"
      :change_hero="change"
      v-if="active_component === 'detail'"
    />
  </main>
</template>

<script>
import '@/static/style.css'
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
      active_component: String,
      last_component: String,
      hero_details: Object,
    }
  },

  methods: {
    show_component(componentName, idHero) {
      if (componentName === 'detail') {
        for (const hero of this.Heroes) {
          if (hero.id === idHero) {
            this.hero_details = hero
            this.active_component = componentName
            return
          }
        }
      }
      this.last_component = componentName
      this.active_component = componentName
    },

    back() {
      this.active_component = this.last_component
    },

    change(name, id) {
      if (name !== '') {
        for (const heroIdx in this.Heroes) {
          const hero = this.Heroes[heroIdx]
          if (hero.id === id) {
            this.Heroes[heroIdx].heroName = name
            this.active_component = this.last_component
            return
          }
        }
      }
    },
  },
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
