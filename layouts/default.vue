<template>
  <v-app dark>
    <v-navigation-drawer
      v-model="mini"
      :mini-variant.sync="mini"
      :clipped="clipped"
      fixed
      app
      permanent
    >
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
            <v-divider></v-divider>
      </v-list>
    </v-navigation-drawer>
    <v-app-bar
      :clipped-left="clipped"
      fixed
      app
    >
      
      <v-app-bar-nav-icon @click.stop="drawer = !drawer" />
      <v-toolbar>
        <img
        :src="require('../static/ytlogo.png')"
        height="23"
        />
          Youtube
        </v-toolbar>
          <v-text-field
            dense
            solo
            label="Search"
            outlined
            flat
          ></v-text-field>
        <v-btn
              icon
            >
              <v-icon>mdi-magnify</v-icon>
            </v-btn>
            <v-btn
              icon
            >
              <v-icon>mdi-microphone</v-icon>
            </v-btn>
          
      <v-spacer />
      <v-btn
              icon
            >
              <v-icon>mdi-apps</v-icon>
      </v-btn>
      <v-btn
              icon
            >
              <v-icon>mdi-dots-vertical</v-icon>
      </v-btn>

      <v-btn
        outlined
        color="blue"
        @click.stop="rightDrawer = !rightDrawer"
      >
        <v-icon>mdi-account</v-icon>
        SIGN IN
      </v-btn>
    </v-app-bar>
    <v-main>
      <v-container>
        <v-row
        justify="space-around"
        align="center"
        >
        <v-chip :input-value="active" filter>All</v-chip>
        <v-chip :input-value="active" filter>Deep House</v-chip>
        <v-chip :input-value="active" filter>Chill-out music</v-chip>
        <v-chip :input-value="active" filter>Blues rock music</v-chip>
        <v-chip :input-value="active" filter>Background music</v-chip>
        <v-chip :input-value="active" filter>Coldplay</v-chip>
        <v-chip :input-value="active" filter>Music</v-chip>
        <v-chip :input-value="active" filter>Greatest hits albums</v-chip>
        <v-chip :input-value="active" filter>Live</v-chip>
        <v-chip :input-value="active" filter>Scorpios</v-chip>
        <v-chip :input-value="active" filter>Radios</v-chip>
        <v-chip :input-value="active" filter>Reggae</v-chip>
        <v-chip :input-value="active" filter>Classic</v-chip>
        </v-row>
      </v-container>
    </v-main>
    <v-navigation-drawer
      v-model="rightDrawer"
      :right="right"
      temporary
      fixed
    >
      <v-list>
        <v-list-item @click.native="right = !right">
          <v-list-item-action>
            <v-icon light>
              mdi-repeat
            </v-icon>
          </v-list-item-action>
          <v-list-item-title>Switch drawer (click me)</v-list-item-title>
        </v-list-item>
      </v-list>
    </v-navigation-drawer>
    <v-footer
      :absolute="!fixed"
      app
    >
      <span>&copy; {{ new Date().getFullYear() }}</span>
    </v-footer>
  </v-app>
</template>

<script>
export default {
  data () {
    return {
      clipped: true,
      drawer: false,
      items: [
        { icon: 'mdi-home', title: 'Home', to: '/' },
        { icon: 'mdi-compass-outline', title: 'Explore',  to: '/' },
        { icon: 'mdi-youtube-subscription', title: 'Subscriptions', to: '/' },
        { icon: 'mdi-play-box-multiple', title: 'Library', to: '/' },
        { icon: 'mdi-history', title: 'History', to: '/' } ],
      miniVariant: true,
      right: true,
      rightDrawer: false,
      title: 'Vuetify.js'
    }
  }
}
</script>

<style> 

</style>
