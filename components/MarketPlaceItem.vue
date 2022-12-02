<template>
  <div>
    <v-container>
      <v-card max-width="250" height="450" elevation="2">
        <v-col>
          <div>
            <p class="description">{{ data.title }}</p>
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
