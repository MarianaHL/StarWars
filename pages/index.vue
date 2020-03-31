<template>
  <v-container>
    <v-row>
      <v-col cols="12">
        Titulo
      </v-col>
      <v-col cols="12">
        Buscador
      </v-col>
    </v-row>
    <v-row>
      <v-col cols="12">
        Menu
      </v-col>
      <v-col cols="12">
        <cards-list
          :list-of-items="characters"
        />
      </v-col>
    </v-row>
  </v-container>
</template>

<script>
import CardsList from '~/components/CardsList'
export default {
  components: {
    CardsList
  },

  async asyncData ({ $axios }) {
    const { data } = await $axios.$get('characters?apikey=09cc91a7f9072e534000cf11ac56e109&ts=1585695057&hash=6938dd66ca4c564da4a7b48aaf141a96')
    return {
      characters: data.results
    }
  }
}
</script>
