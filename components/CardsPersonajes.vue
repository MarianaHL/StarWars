<template>
  <v-card
    class="mx-auto"
    max-width="400"
  >
    <v-img
      class="white--text align-end"
      height="200px"
      :src="imageName"
    >
      <!-- /<v-card-title></v-card-title> -->
    </v-img>

    <v-card-title class="pb-0">
      {{ item.name }}
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
  },

  computed: {
    imageName () {
      return `${this.item.thumbnail.path}/standard_xlarge.${this.item.thumbnail.extension}`
    }
  }
}
</script>
