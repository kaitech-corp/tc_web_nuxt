<template>
  <v-col>
    <BannerItem />
    <IntroSection
      v-for="section in introDataInfo"
      :key="section.id"
      :data="section"
    />
    <FeatureSection
      v-for="feature in featureData"
      :key="feature.id"
      :data="feature"
    />
    <HighlightSection v-if="!$vuetify.breakpoint.mobile" :data="highlightsData[0]" />
    <HighlightCarousel v-if="$vuetify.breakpoint.mobile" :data="highlightsData[0].cards"/>
    <TestimonialSection :data="testomonialsData[0]" />
  </v-col>
</template>

<script>
import { introData, features, highlights, testomonials } from '@/assets/data.js'
export default {
  name: 'IndexPage',
  data() {
    return {
      introDataInfo: introData,
      featureData: features,
      highlightsData: highlights,
      testomonialsData: testomonials,
    }
  },
}
</script>
