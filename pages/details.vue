<template>
  <v-container>
    <v-row>
      <v-col cols="12" class="d-flex justify-center">
        <v-img
          src="/logoMarvel.png"
          width="40%"
          max-width="40%"
        />
      </v-col>
    </v-row>
    <v-row>
      <v-col>
        <card-films
          :item-details="item"
        />
      </v-col>
    </v-row>
  </v-container>
</template>

<script>
import CardFilms from '~/components/CardFilms'
export default {
  components: {
    CardFilms
  },

  asyncData ({ params, redirect }) {
    if (!params.item) {
      redirect({ path: '/' })
    }
    return {
      item: params.item
    }
  }
}
</script>
