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

        
        <v-list-item
          v-for="(item1, i) in items1"
          :key="i"
          :to="item1.to"
          router
          exact
        >
            <v-list-item-action>
            <v-icon>{{ item1.icon1 }}</v-icon>
          </v-list-item-action>
          <v-list-item-content>
            <v-list-item-title v-text="item1.title1" />
          </v-list-item-content>
          </v-list-item>

         <v-divider></v-divider>

        <v-list-item
          v-for="(item2, i) in items2"
          :key="i"
          :to="item2.to"
          router
          exact
        >
         <v-list-item-action>
            <v-list-item-title v-text="item2.text" />
            <v-icon>{{ item2.icon2 }}</v-icon>
          </v-list-item-action>
          <v-list-item-content>
            <v-list-item-title v-text="item2.title2" />
          </v-list-item-content>
          </v-list-item>

         <v-divider></v-divider>

        <v-list-item
          v-for="(item3, i) in items3"
          :key="i"
          :to="item3.to"
          router
          exact
        >
         <v-list-item-action>
           <v-list-item-title v-text="item3.text3" />
            <v-icon>{{ item3.icon3 }}</v-icon>
          </v-list-item-action>
          <v-list-item-content>
            <v-list-item-title v-text="item3.title3" />
          </v-list-item-content>
          </v-list-item>

         <v-divider></v-divider>

        <v-list-item
          v-for="(item4, i) in items4"
          :key="i"
          :to="item4.to"
          router
          exact
        >
         <v-list-item-action>
            <v-icon>{{ item4.icon4 }}</v-icon>
          </v-list-item-action>
          <v-list-item-content>
            <v-list-item-title v-text="item4.title4" />
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
        { icon: 'mdi-youtube-subscription', title: 'Subscriptions', to: '/##' },
        ],
        items1: [
        { icon1: 'mdi-play-box-multiple', title1: 'Library', to: '/###' },
        { icon1: 'mdi-history', title1: 'History', to: '/####' },
        ],
        items2: [
        { text: 'Sign in to like videos,' },
        { text: 'comment, and subscribe.' },
        { icon2: 'mdi-account', title2: 'SIGN IN', to: '/#####' },
        ],
        items3: [
        { text3: 'BEST OF YOUTUBE', to: '/######' },
        { icon3: 'mdi-music', title3: 'Music', to: '/########' },
        { icon3: 'mdi-trophy-variant', title3: 'Sports', to: '/#########' },
        { icon3: 'mdi-youtube-gaming', title3: 'Gaming', to: '/##########' },
        { icon3: 'mdi-newspaper-variant-outline', title3: 'News', to: '/###########' },
        { icon3: 'mdi-access-point', title3: 'Live', to: '/############' },
        { icon3: 'mdi-panorama-sphere-outline', title3: '360 Video', to: '/#############' },
        ],
        items4: [
        { icon: 'mdi-plus-circle-outline', title4: 'Browse channels', to: '/##############' },
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
