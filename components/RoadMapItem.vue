<template>
  <div>
    <v-container>
      <v-card width="450" elevation="3" class="pa-4">
        <div>
          <h4 class="heading">{{ data.title }}</h4>
        </div>
        <div>
          <p class="description">{{ data.description }}</p>
        </div>
        <div>
          <p class="date">{{ data.date }}</p>
        </div>
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
  font-size: 28px;
  line-height: 36px;
  font-weight: 600;
  color: black;
  text-align: center;
}

.description {
  font-size: 20px;
  line-height: 32px;
  color: black;
  text-align: center;
}

.date {
  font-size: 20px;
  line-height: 32px;
  font-weight: 500;
  text-align: center;
}
</style>
