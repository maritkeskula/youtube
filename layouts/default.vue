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
            <v-list-item-title class="text-subtitle-2" v-text="item.text" />
            <v-icon>{{ item.icon }}</v-icon>
          </v-list-item-action>
          <v-list-item-content>
            <v-list-item-title class="text-subtitle-2" v-text="item.title" />
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
            outlined
            class="d-flex align-center mt-6"
            >
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
        <v-chip-group>
        <v-chip  class="ma-2" @click="active" filter>All</v-chip>
        <v-chip  class="ma-2" @click="active" filter>Deep House</v-chip>
        <v-chip  class="ma-2" @click="active" filter>Chill-out music</v-chip>
        <v-chip  class="ma-2" @click="active" filter>Blues rock music</v-chip>
        <v-chip  class="ma-2" @click="active" filter>Background music</v-chip>
        <v-chip  class="ma-2" @click="active" filter>Coldplay</v-chip>
        <v-chip  class="ma-2" @click="active" filter>Music</v-chip>
        <v-chip  class="ma-2" @click="active" filter>Greatest hits albums</v-chip>
        <v-chip  class="ma-2" @click="active" filter>Live</v-chip>
        <v-chip  class="ma-2" @click="active" filter>Scorpios</v-chip>
        <v-chip  class="ma-2" @click="active" filter>Radios</v-chip>
        <v-chip  class="ma-2" @click="active" filter>Reggae</v-chip>
        <v-chip  class="ma-2" @click="active" filter>Classic</v-chip>
        <v-chip  class="ma-2" @click="active" filter>All</v-chip>
        <v-chip  class="ma-2" @click="active" filter>Deep House</v-chip>
        <v-chip  class="ma-2" @click="active" filter>Chill-out music</v-chip>
        <v-chip  class="ma-2" @click="active" filter>Blues rock music</v-chip>
        <v-chip  class="ma-2" @click="active" filter>Background music</v-chip>
        <v-chip  class="ma-2" @click="active" filter>Coldplay</v-chip>
        <v-chip  class="ma-2" @click="active" filter>Music</v-chip>
        <v-chip  class="ma-2" @click="active" filter>Greatest hits albums</v-chip>
        <v-chip  class="ma-2" @click="active" filter>Live</v-chip>
        <v-chip  class="ma-2" @click="active" filter>Scorpios</v-chip>
        <v-chip  class="ma-2" @click="active" filter>Radios</v-chip>
        <v-chip  class="ma-2" @click="active" filter>Reggae</v-chip>
        <v-chip  class="ma-2" @click="active" filter>Classic</v-chip>
        </v-chip-group>
        </v-row>
      </v-container>
    
<v-row no-gutters>
      <v-col
        v-for="n in 3"
        :key="n"
        cols="12"
        sm="4"
      >
<v-card
    class="mx-auto ma-5"
    max-width="300"
    
  >
    <v-img
      src="https://loremflickr.com/300/180"
    ></v-img>

    <v-card-title>
      Me at the zoo
    </v-card-title>

    <v-card-subtitle>
      jawed
       </v-card-subtitle>
       <v-card-subtitle>
      230M views | 16 years ago
      </v-card-subtitle>
  </v-card>

<v-card
    class="mx-auto ma-5"
    max-width="300"
    
  >
    <v-img
      src="https://picsum.photos/300/180?random"
    ></v-img>

    <v-card-title>
      Johnny Knoxville Breaks Down every injury of his career
    </v-card-title>

    <v-card-subtitle>
      Vanity Fair
       </v-card-subtitle>
       <v-card-subtitle>
      33M views | 3 years ago
      </v-card-subtitle>
  </v-card>

  <v-card
    class="mx-auto ma-5"
    max-width="300"
    
  >
    <v-img
      src="https://picsum.photos/300/180"
    ></v-img>

    <v-card-title>
      Relaxing christmas jazz music 10 hours
    </v-card-title>

    <v-card-subtitle>
      relax cafe music
       </v-card-subtitle>
       <v-card-subtitle>
      5.7M views | 1 year ago
      </v-card-subtitle>
  </v-card>

<v-card
    class="mx-auto ma-5"
    max-width="300"
    
  >
    <v-img
      src="	https://source.unsplash.com/user/c_v_r/300x180"
    ></v-img>

    <v-card-title>
      Keanu Reeves and Carrie-Anne
    </v-card-title>

    <v-card-subtitle>
      The Verge
       </v-card-subtitle>
       <v-card-subtitle>
      1.4M views | 5 days ago
      </v-card-subtitle>
  </v-card>

  </v-col>
  </v-row>

</v-main>
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
        { icon: 'mdi-access-point', title: 'Live', to: '/#10' },
        { icon: 'mdi-panorama-sphere-outline', title: '360 Video', to: '/#11' },
        <divider></divider>,
        { icon: 'mdi-plus-circle-outline', title: 'Browse channels', to: '/#12' },
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
