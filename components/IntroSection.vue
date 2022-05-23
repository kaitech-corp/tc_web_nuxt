<template>
  <div class="ma-6 pb-4 bgColor">
    <v-container>
      <v-layout row no-gutters justify-center align-center>
        <v-col class="pb-4">
          <div>
            <h1 class="header" style="text-align: center">
              {{ data.header }}
            </h1>
          </div>
          <div>
            <p class="description" style="text-align: center">
              {{ data.description }}
            </p>
            <p class="description" style="text-align: center">
              {{ data.description2 }}
            </p>
          </div>
        </v-col>
        <div align="center">
          <v-img
            :max-width="$vuetify.breakpoint.mobile ? 400 : 600"
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
}
</script>

<style scoped>
.header {
  font-size: 48px;
  line-height: 68px;
  font-weight: 600;
}

.description {
  font-size: 25px;
  line-height: 32px;
  font-weight: 500;

  /* font-family: monospace; */
}

.download-button {
  display: inline-flex;
}
</style>
