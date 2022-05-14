<template>
  <div>
    <v-hover v-slot="{ hover }" close-delay="200">
      <v-banner
        align="center"
        single-line
        color="#0052ff"
        :elevation="hover ? 8 : 2"
        :class="{ 'on-hover': hover }"
      >
        <button @click="isVisible = !isVisible">
          Join the wait list for special access to XplorChain→
        </button>
      </v-banner>
    </v-hover>
    <v-col align="center">
      <v-alert v-if="isVisible" class="d-inline-flex justify-center">
        <v-form>
          <v-card elevation="2" outlined class="mx-auto pa-2 grey lighten-4">
            <v-text-field
              label="Subscribe!"
              placeholder="Email"
              type="email"
              solo
            ></v-text-field>
            <v-btn color="blue" elevation="2" @click="isVisible = !isVisible">Submit</v-btn>
          </v-card>
        </v-form>
      </v-alert>
    </v-col>
  </div>
</template>

<script>
export default {
  name: 'BannerItem',
  data() {
    return {
      isVisible: false,
    }
  },
}
</script>

<style scoped>
.banner {
  display: flex;
  align-items: center;
  justify-content: center;
  height: 37px;
  background-color: #0052ff;
  cursor: pointer;
}

.banner-text {
  /* font-family: Helvetica; */
  font-size: 16px;
  line-height: 19px;
  font-weight: 500;
}

.v-banner.on-hover.theme-dark {
  background: grey;
}
</style>
