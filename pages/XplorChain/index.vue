<template>
  <div>
    <BannerItem />
    <IntroSection :data="xplorData[0]" />
    <MarketSection :data="marketPlaceData[0]" />
  </div>
</template>

<script>
import { xplorchain, marketplace } from '@/assets/data.js'
export default {
  name: 'IndexPage',
  data() {
    return {
      xplorData: xplorchain,
      marketPlaceData: marketplace,
    }
  },
}
</script>

<style lang="sass" scoped>
</style>