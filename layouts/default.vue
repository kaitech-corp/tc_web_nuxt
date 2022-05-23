<template>
  <v-app name="tc">
    <v-navigation-drawer
      v-model="drawer"
      disable-resize-watcher
      :mini-variant="miniVariant"
      :clipped="clipped"
      fixed
      temporary
    >
      <TCLogo class="ma-2" />
      <v-list>
        <v-list-item
          v-for="(item, i) in items"
          :key="i"
          :to="item.to"
          router
          exact
        >
          <v-list-item-action>
            <v-icon>{{ item.icon }}</v-icon>
          </v-list-item-action>
          <v-list-item-content>
            <v-list-item-title v-text="item.title" />
          </v-list-item-content>
        </v-list-item>
      </v-list>
    </v-navigation-drawer>

    <v-toolbar>
      <v-app-bar-nav-icon @click.stop="drawer = !drawer" />
      <v-col align="end">
        <button
          v-if="!$vuetify.breakpoint.mobile"
          class="button-primary"
          @click="getDeviceType"
        >
          <v-icon color="white">mdi-download</v-icon> Download Now!
        </button>
        <v-btn v-if="$vuetify.breakpoint.mobile" icon @click="getDeviceType">
          <v-icon>mdi-download</v-icon>
        </v-btn>
      </v-col>
    </v-toolbar>

    <v-main>
      <Nuxt />
    </v-main>
    <v-footer absolute app>
      <v-container>
        <v-col align="center">
          <v-row no-gutters justify="space-between">
            <div class="ma-2">
              <v-btn
                v-for="link in links"
                :key="link.id"
                color="black"
                text
                rounded
                class="my-2"
              >
                <NuxtLink :to="link.route">{{ link.text }}</NuxtLink>
              </v-btn>
            </div>
            <v-col align="center">
            <div class="ma-2">
              <v-btn
                v-for="icon in icons"
                :key="icon.id"
                class="mx-2 black--text"
                icon
                elevation="2"
                :href="icon.link"
              >
                <v-icon size="24px">
                  {{ icon.icon }}
                </v-icon>
              </v-btn>
            </div>
            </v-col>
          </v-row>
          <span class="ma-2"
            >&copy; {{ new Date().getFullYear() }} Kai Technologies Corp</span
          >
        </v-col>
      </v-container>
    </v-footer>
  </v-app>
</template>

<script>
export default {
  name: 'DefaultLayout',
  data() {
    return {
      clipped: false,
      drawer: false,
      fixed: true,
      items: [
        {
          icon: 'mdi-home',
          title: 'Home',
          to: '/',
        },
        {
          icon: 'mdi-chart-bubble',
          title: 'XplorChain',
          to: 'XplorChain',
        },
        {
          icon: 'mdi-apps',
          title: 'Privacy Policy',
          to: '/privacy-policy',
        },
        {
          icon: 'mdi-chart-bubble',
          title: 'Terms & Conditions',
          to: '/terms-conditions',
        },
      ],
      miniVariant: false,
      right: false,
      rightDrawer: false,
      title: 'Travel Crew',
      selectedItem: 1,
      links: [
        { text: 'Home', route: '/' },
        { text: 'Privacy Policy', route: 'privacy-policy' },
        { text: 'Terms and Conditions', route: 'terms-conditions' },
        { text: 'Contact Us', route: '' },
      ],
      icons: [
        { icon: 'mdi-facebook', link: 'https://fb.me/TravelCrew.KT' },
        { icon: 'mdi-twitter', link: 'https://twitter.com/TravelCrew_kt' },
        {
          icon: 'mdi-instagram',
          link: 'https://www.instagram.com/travelcrew_kt/',
        },
      ],
    }
  },
  methods: {
    getDeviceType() {
      if (navigator.userAgent.toLowerCase().includes('android') > -1) {
        window.location.href =
          'https://play.google.com/store/apps/details?id=com.kaitechcorp.travelcrew'
      }
      if (navigator.userAgent.toLowerCase().includes('iphone') > -1) {
        window.location.href =
          'https://apps.apple.com/us/app/travel-crew/id1501930493'
      }
    },
  },
}
</script>
<style scoped>
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
