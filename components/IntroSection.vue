<template>
  <div class="ma-6 pb-4 bgColor">
    <v-container>
      <v-layout row no-gutters justify-center align-center>
        <v-col>
          <div>
            <h1 class="header">
              {{ data.header }}
            </h1>
          </div>
          <div>
            <p class="description">{{ data.description }}</p>
            <p class="description">{{ data.description2 }}</p>
          </div>
          <div>
            <button class="button-primary">Download Now!</button>
          </div>
        </v-col>
        <div align="center">
          <v-img
            :src="require(`@/assets/images/${data.image || 'web1.png'}`)"
            alt="app image"
            class="image"
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
  /* width: 25%; */
  max-width: 600px;
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

  /* font-family: monospace; */
}

.download-button {
  display: inline-flex;
}

.button-primary {
  position: relative;
  width: auto;
  border-radius: 4px;
  font-weight: 500;
  color: #fff;
  cursor: pointer;

  /* font-family: "Helvetica Neue"; */
  padding: 10px 12px;
  font-size: 14px;
  line-height: 14px;
  border: 1px solid #0052ff;
  background-color: #0052ff;
}
</style>
