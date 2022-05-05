<template>
  <div>
    <v-container v-if="data.id">
      
      <v-layout row no-gutters justify-space-between align-center>
        <div style="width: 50%">
          <v-col >
            <div>
              <h1 class="header">
                {{ data.header }}
              </h1>
            </div>
            <div>
              <p class="description">{{ data.description }}</p>
            </div>
          </v-col>
        </div>
        <div class="image">
          <v-img
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