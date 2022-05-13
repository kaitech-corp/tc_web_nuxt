<template>
  <div>
    <v-container>
      <v-card max-width="250" height="450" elevation="2">
        <v-col>
          <div>
            <h4 class="heading">{{ data.title }}</h4>
          </div>
          <div>
            <p class="description">{{ data.description }}</p>
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
.heading {
  font-size: 32px;
  line-height: 36px;
  font-weight: 500;
  color: black;
  text-align: center;
}

.description {
  font-size: 20px;
  line-height: 32px;
  color: black;
  text-align: center;
}
</style>
