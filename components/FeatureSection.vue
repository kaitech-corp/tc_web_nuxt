<template>
  <div>
    <v-container>
      <v-col align="center">
        <div>
          <h1 class="header">
            {{ data.header }}
          </h1>
        </div>
        <div>
          <p class="description">{{ data.description }}</p>
        </div>
      </v-col>
      <FeaturesItem
        v-for="feature in data.cards"
        :key="feature.id"
        :data="feature"
      />
    </v-container>
  </div>
</template>

<script>
export default {
  props: {
    data: {
      type: Object,
      default: null,
    },
  },
}
</script>

<style lang="scss" scoped>
.header {
  font-size: 61px;
  line-height: 68px;
  font-weight: 400;
}

.description {
  font-size: 25px;
  line-height: 32px;
  font-weight: 500;
  color: rgb(56, 122, 236);

  /* font-family: monospace; */
}
</style>