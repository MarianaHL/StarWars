<template>
  <v-row>
    <v-col
      v-for="item of listOfItems"
      :key="item.name"
      cols="3"
    >
      <card-personajes
        :item="item"
      />
    </v-col>
  </v-row>
</template>

<script>
import CardPersonajes from '~/components/CardsPersonajes'
export default {
  components: {
    CardPersonajes
  },

  props: {
    listOfItems: {
      type: Array,
      default: () => []
    }
  }
}
</script>
