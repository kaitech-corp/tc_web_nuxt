<template>
  <div class="blue lighten-5">
    
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
      <HighlightItem :data="data.cards" />
      
    
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
.image {
  max-width: 400px;

  // max-width: 400px;
}

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