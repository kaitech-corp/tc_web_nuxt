<template>
  <div>
    <v-row v-for="line in data" :key="line">
      <p style="text-align: justify">{{ line }}</p>
    </v-row>
  </div>
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

<style lang="scss" scoped></style>
