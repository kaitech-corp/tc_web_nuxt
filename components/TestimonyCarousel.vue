<template>
  <v-row justify="center">
    <v-expansion-panels inset>
      <v-expansion-panel v-for="highlight in data" :key="highlight.id">
        <v-expansion-panel-header>
          {{ highlight.name }}
        </v-expansion-panel-header>
        <v-expansion-panel-content>
          {{ highlight.description }}
        </v-expansion-panel-content>
      </v-expansion-panel>
    </v-expansion-panels>
  </v-row>
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
.description {
  font-size: 20px;
  line-height: 32px;
  font-weight: 400;

  /* font-family: monospace; */
  color: black;
  text-align: center;
}
</style>
