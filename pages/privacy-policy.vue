<template>
  <v-container>
    <div>
      <h1 class="ma-6 pb-2" style="text-align: center">
        {{ policyInfo.title }}
      </h1>
      <v-spacer></v-spacer>
      <PolicyItem :data="policyInfo.description" />
    </div>
  </v-container>
</template>

<script>
import { policy } from '@/assets/data.js'
export default {
  data() {
    return {
      policyInfo: policy,
    }
  },
}
</script>

<style lang="scss" scoped></style>
