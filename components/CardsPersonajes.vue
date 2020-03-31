<template>
  <v-card
    class="mx-auto"
    max-width="400"
  >
    <v-img
      class="white--text align-end"
      height="200px"
      src=""
    >
      <!-- /<v-card-title></v-card-title> -->
    </v-img>

    <v-card-title class="pb-0">
      {{ item.title }}
    </v-card-title>
  </v-card>
</template>

<script>
export default {
  props: {
    item: {
      type: Object,
      default: () => {}
    }
  }
}
</script>
