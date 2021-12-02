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
            <v-list-item-title v-text="item.text" />
            <v-icon>{{ item.icon }}</v-icon>
          </v-list-item-action>
          <v-list-item-content>
            <v-list-item-title v-text="item.title" />
          </v-list-item-content>
        </v-list-item>
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
            outlined>
            </v-text-field>
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
      <v-container
        height: 50px
        color: grey darken-4
        >
        <v-row
        justify="space-around"
        align="center"
        justify-content="center"
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
  </v-app>
</template>

<script>
export default {
  data () {
    return {
      clipped: true,
      drawer: true,
      items: [
        { icon: 'mdi-home', title: 'Home', to: '/' },
        { icon: 'mdi-compass-outline', title: 'Explore',  to: '/#' },
        { icon: 'mdi-youtube-subscription', title: 'Subscriptions', to: '/#1' },
        <divider></divider>,
        { icon: 'mdi-play-box-multiple', title: 'Library', to: '/#2' },
        { icon: 'mdi-history', title: 'History', to: '/#3' },
        <divider></divider>,
        { text: 'Sign in to like videos,' },
        { text: 'comment, and subscribe.' },
        { icon: 'mdi-account', title: 'SIGN IN', to: '/#4' },
        <divider></divider>,
        { text: 'BEST OF YOUTUBE', to: '/#5' },
        { icon: 'mdi-music', title: 'Music', to: '/#6' },
        { icon: 'mdi-trophy-variant', title: 'Sports', to: '/#7' },
        { icon: 'mdi-youtube-gaming', title: 'Gaming', to: '/#8' },
        { icon: 'mdi-newspaper-variant-outline', title: 'News', to: '/#9' },
        { icon: 'mdi-access-point', title: 'Live', to: '/#11' },
        { icon: 'mdi-panorama-sphere-outline', title: '360 Video', to: '/#12' },
        <divider></divider>,
        { icon: 'mdi-plus-circle-outline', title: 'Browse channels', to: '/#13' },
      ],
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
