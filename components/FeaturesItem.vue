<template>
  <div>
    <v-container v-if="data.id" class="my-4">
      <v-layout row no-gutters justify-center align-center>
        <v-col class="pb-4">
          <div :style="{ width: width }">
            <div>
              <h1 class="header" style="text-align: center">
                {{ data.header }}
              </h1>
            </div>
            <div>
              <p class="description" style="text-align: center">
                {{ data.description }}
              </p>
            </div>
          </div>
        </v-col>
        <div align="center">
          <v-img
            :max-width="$vuetify.breakpoint.xs || $vuetify.breakpoint.sm ? 400 : 500"
            :src="require(`@/assets/images/${data.image || 'web1.png'}`)"
            alt="app image"
          ></v-img>
        </div>
      </v-layout>
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
  computed: {
    width() {
        return this.$vuetify.breakpoint.xs || this.$vuetify.breakpoint.sm ? "100%" : "75%"
    },
  },
}
</script>

<style scoped>
.image {
  width: 25%;

  /* max-width: 400px; */
}

.description {
  font-size: 25px;
  line-height: 32px;
  font-weight: 400;

  /* font-family: monospace; */
  color: black;
  text-align: center;
}

.header {
  font-size: 37px;
  line-height: 40px;
  font-weight: 400;
  text-align: center;
  color: #387aec;

  /* font-family: monospace; */
}
</style>
