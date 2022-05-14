<template>
  <div>
    <BannerItem />
    <IntroSection :data="xplorData[0]" />
    <MarketSection :data="marketPlaceData[0]" />
    <RoadMap :data="roadMapData[0]" />
    <CreatorsCorner :data="creatorsData[0]" />
  </div>
</template>

<script>
import { xplorchain, marketplace, roadMap, creators } from '@/assets/data.js'
export default {
  name: 'IndexPage',
  data() {
    return {
      xplorData: xplorchain,
      marketPlaceData: marketplace,
      roadMapData: roadMap,
      creatorsData: creators,
    }
  },
}
</script>

<style lang="sass" scoped></style>
