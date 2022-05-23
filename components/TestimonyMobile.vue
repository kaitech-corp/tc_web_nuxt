<template>
  <div :data="data">
    <v-col
      v-touch="{ left: () => swipe('Left'), right: () => swipe('Right') }"
      align="center"
    >
      <TestimoniaItem :key="data[index].id" :data="data[index]" />
    </v-col>
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
  data: () => ({
    swipeDirection: 'None',
    index: 0,
  }),

  methods: {
    swipe(direction) {
      this.swipeDirection = direction
      if (direction === 'Left') {
        const i = this.index + 1
        if (i < 4) {
          this.index = i
        } else {
          this.index = 0
        }
      } else if (direction === 'Right') {
        const i = this.index - 1
        if (i < 0) {
          this.index = -i
        }
      }
    },
  },
}
</script>

<style lang="scss" scoped></style>
