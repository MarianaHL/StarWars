<template>
  <v-card
    color="#400D0D"
    dark
    class="card__film"
  >
    <div class="d-flex flex-no-wrap justify-space-between">
      <div>
        <v-card-title
          class="headline"
          v-text="itemDetails.name"
        />
        <v-card-subtitle>
          Numero de comics {{ itemDetails.comics.available }}
        </v-card-subtitle>
        <v-card-subtitle>
          Numero de series en las que aparece {{ itemDetails.series.available }}
        </v-card-subtitle>
      </div>

      <v-avatar
        class="ma-3"
        size="300"
        tile
      >
        <v-img :src="imageName" />
      </v-avatar>
    </div>
  </v-card>
</template>

<script>
export default {
  props: {
    itemDetails: {
      type: Object,
      required: true
    }
  },

  computed: {
    imageName () {
      return `${this.itemDetails.thumbnail.path}/standard_xlarge.${this.itemDetails.thumbnail.extension}`
    }
  }
}
</script>

<style scoped>
.card__film {
  height: 350px;
}
</style>
