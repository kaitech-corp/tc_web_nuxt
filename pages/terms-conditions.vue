<template>
<v-container>
  <div>
    <h1 class="ma-6 pb-2" style="text-align:center">{{ termsInfo.title }}</h1>
    <v-spacer></v-spacer>
    <h4 class="ma-6 pb-2" style="text-align:center">{{ termsInfo.subtitle }}</h4>
    <PolicyItem 
    :data="termsInfo.description" />
  </div>
</v-container>
</template>

<script>
import { terms } from '@/assets/data.js'
export default {
  data() {
    return {
      termsInfo: terms,
    }
  },
}
</script>

<style lang="scss" scoped>
</style>