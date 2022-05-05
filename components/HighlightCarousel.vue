<template>
  <v-card rounded elevation="24" max-width="444" class="mx-auto">
    <v-carousel
    cycle=true
    continuous=true
    >
      <v-carousel-item v-for="highlight in data" :key="highlight.id">
        <v-img
          :src="require(`@/assets/images/${highlight.image || 'web1.png'}`)"
          alt="app image"
          class="image"
        ></v-img>
        <v-card-title>
          {{ highlight.header }}
        </v-card-title>
        <v-card-subtitle align="start">
          {{ highlight.description }}
        </v-card-subtitle>
      </v-carousel-item>
    </v-carousel>
  </v-card>
</template>

<script>
export default {
  props: {
    data: {
      type: Array,
      default: null,
    },
  },
}
</script>

<style scoped>
.image {
  /* width: 25%; */
  max-height: 400px;
}
</style>