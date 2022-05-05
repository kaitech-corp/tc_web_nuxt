<template>
  <div>
    <v-container>
      <v-card max-width="250" height="450" elevation="2">
        <v-col>
          <div>
            <p class="description">{{ data.description }}</p>
          </div>
          <div>
            <p class="description">{{ data.name }}</p>
          </div>
        </v-col>
      </v-card>
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
.description {
  font-size: 20px;
  line-height: 32px;
  font-weight: 400;

  /* font-family: monospace; */
  color: black;
  text-align: center;
}
</style>