<template>
  <v-app>
    <v-app-bar :clipped-left="clipped" fixed app>
      <v-spacer />
      <NuxtLink to="/">
        <v-btn icon>
          <font-awesome-icon icon="home" />
        </v-btn>
      </NuxtLink>
      <NuxtLink to="/accomodation">
        <v-btn icon>
          <font-awesome-icon icon="campground" />
        </v-btn>
      </NuxtLink>
      <NuxtLink to="/location">
        <v-btn icon>
          <font-awesome-icon icon="map-marked-alt" />
        </v-btn>
      </NuxtLink>
      <NuxtLink to="/contact">
        <v-btn icon>
          <font-awesome-icon icon="address-card" />
        </v-btn>
      </NuxtLink>
      <NuxtLink to="/details">
        <v-btn icon>
          <font-awesome-icon icon="clipboard-list" />
        </v-btn>
      </NuxtLink>
      <NuxtLink to="/reception">
        <v-btn icon>
          <font-awesome-icon icon="glass-cheers" />
        </v-btn>
      </NuxtLink>
      <v-btn icon @click.stop="rightDrawer = !rightDrawer">
        <v-icon>mdi-menu</v-icon>
      </v-btn>
    </v-app-bar>
    <Nuxt />
    <v-navigation-drawer v-model="rightDrawer" :right="right" temporary fixed>
      <v-list>
        <v-list-item NuxtLink to="/">
          <v-list-item-action>
            <font-awesome-icon icon="home" />
          </v-list-item-action>
          <v-list-item-title>Home</v-list-item-title>
        </v-list-item>
        <v-list-item NuxtLink to="/accomodation">
          <v-list-item-action>
            <font-awesome-icon icon="campground" />
          </v-list-item-action>
          <v-list-item-title>Accomodation</v-list-item-title>
        </v-list-item>
        <v-list-item NuxtLink to="/location">
          <v-list-item-action>
            <font-awesome-icon icon="map-marked-alt" />
          </v-list-item-action>
          <v-list-item-title>Location</v-list-item-title>
        </v-list-item>
        <v-list-item NuxtLink to="/contact">
          <v-list-item-action>
            <font-awesome-icon icon="address-card" />
          </v-list-item-action>
          <v-list-item-title>Contact Us</v-list-item-title>
        </v-list-item>
        <v-list-item NuxtLink to="/details">
          <v-list-item-action>
            <font-awesome-icon icon="clipboard-list" />
          </v-list-item-action>
          <v-list-item-title>Full Details</v-list-item-title>
        </v-list-item>
        <v-list-item NuxtLink to="/reception">
          <v-list-item-action>
            <font-awesome-icon icon="glass-cheers" />
          </v-list-item-action>
          <v-list-item-title>Reception</v-list-item-title>
        </v-list-item>
      </v-list>
    </v-navigation-drawer>
    <v-footer :absolute="!fixed" app>
      <span>&copy; {{ new Date().getFullYear() }} Developed by F Galston</span>
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
      fixed: false,
      items: [
        {
          icon: 'mdi-apps',
          title: 'Welcome',
          to: '/',
        },
        {
          icon: 'mdi-chart-bubble',
          title: 'Inspire',
          to: '/inspire',
        },
      ],
      miniVariant: false,
      right: true,
      rightDrawer: false,
    }
  },
}
</script>
