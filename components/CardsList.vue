<template>
  <v-row>
    <v-col
      v-for="item of listOfItems"
      :key="item.name"
      xs="12"
      sm="6"
      md="3"
      lg="2"
      xl="2"
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
