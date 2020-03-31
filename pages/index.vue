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
        <cards-list />
      </v-col>
    </v-row>
  </v-container>
</template>

<script>
import CardsList from '~/components/CardsList'
export default {
  components: {
    CardsList
  }
}
</script>
