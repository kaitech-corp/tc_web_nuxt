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
      >>>>>>> Stashed changes
      <v-app-bar-nav-icon @click.stop="drawer = !drawer" />
      <TCIconLogo />
      <v-col align="end">
        <v-btn plain :to="items[1].to" v-text="items[1].title" />

        <v-btn icon>
          <v-icon>mdi-download</v-icon>
        </v-btn>
      </v-col>
    </v-toolbar>

    <v-main>
      <Nuxt />
    </v-main>
    <v-footer :absolute="!fixed" app>
      <v-container>
        <v-col align="center">
          <v-row no-gutters justify="space-between" align="center">
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
          </v-row>
          <span
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
}
</script>
