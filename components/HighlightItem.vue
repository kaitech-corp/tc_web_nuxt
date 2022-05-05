<template>
  <v-container>
    <v-row>
      <v-col v-for="highlight in data" :key="highlight.id" align="center">
        <v-card elevation="2" rounded-xl max-width="400">
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
        </v-card>
      </v-col>
    </v-row>
  </v-container>
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

<style lang="scss" scoped>
.image {
  /* width: 25%; */
  max-height: 400px;
}
</style>