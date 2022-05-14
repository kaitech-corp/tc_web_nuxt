<template>
  <div class="blue lighten-5">
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
        <div>
          <p class="description">{{ data.description2 }}</p>
        </div>
      </v-col>
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

<style scoped>
.image {
  max-width: 400px;
}

.header {
  font-size: 48px;
  line-height: 68px;
  font-weight: 600;
}

.description {
  font-size: 25px;
  line-height: 32px;
  font-weight: 500;
}
</style>
