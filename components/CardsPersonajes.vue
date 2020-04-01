<template>
  <v-card
    color="#400D0D"
    class="mx-auto"
    max-width="400"
    ripple
    elevation="10"
    @click="onShowDetails"
  >
    <v-img
      class="white--text align-end"
      height="200px"
      :src="imageName"
    >
      <!-- /<v-card-title></v-card-title> -->
    </v-img>

    <v-card-title class="pb-0 title__card">
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
  },

  methods: {
    onShowDetails () {
      console.log('click')
      this.$router.push({
        name: 'details',
        params: {
          item: this.item
        }
      })
    }
  }
}
</script>

<style scoped>
.title__card {
  color: aliceblue
}
</style>
