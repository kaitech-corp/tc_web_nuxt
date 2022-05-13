<template>
  <div>
    <v-container>
      <v-col align="center">
        <div>
          <h1 class="header">
            {{ data.header }}
          </h1>
        </div>
        <div>
          <p class="description">{{ data.description }}</p>
        </div>
      </v-col>
      <v-container>
        <v-row v-for="(j, index) in justify" :key="j" :justify="j">
          <v-col v-for="k in 1" :key="k" md="6">
            <transition name="bounce">
              <RoadMapItem :data="data.cards[index]"></RoadMapItem>
            </transition>
          </v-col>
        </v-row>
      </v-container>
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
  data: () => ({
    justify: ['start', 'end', 'start', 'end', 'start'],
  }),
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

.bounce-enter-from {
  opacity: 0;
}

.bounce-enter-active {
  transition: all 2s ease;
}

/* .bounce-leave-to {
    opacity: 0
} */
</style>
