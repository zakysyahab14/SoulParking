<template>
  <no-ssr>
    <div>
      <div>
        <v-app dark>
          <v-navigation-drawer
            v-model="drawer"
            :mini-variant="miniVariant"
            :clipped="clipped"
            fixed
            app
          >
            <v-list>
            <v-list-item>
            <v-list-item-avatar>
              <img src="https://randomuser.me/api/portraits/men/81.jpg">
            </v-list-item-avatar>

            <v-list-item-content>
              <v-list-item-title>SOUL PARKING TEST</v-list-item-title>
              <v-list-item-subtitle>Abdullah Zaky</v-list-item-subtitle>
            </v-list-item-content>
          </v-list-item>
          </v-list>
            <v-list>
              <div>
              <v-list-item href="/dashboard">
                <v-list-item-icon>
                  <v-icon>mdi-view-dashboard</v-icon>
                </v-list-item-icon>

                <v-list-item-title >Dashboard</v-list-item-title>
              </v-list-item>

              <v-list-group
                value="true"
              >
                <template v-slot:activator>
                  <v-list-item-icon>
                  <v-icon>mdi-cog</v-icon>
                </v-list-item-icon>
                  <v-list-item-title>Pengaturan Lokasi</v-list-item-title>
                </template>
                  <v-list-item
                    v-for="(sub, i) in subItem"
                    :key="i"
                    :to="sub[1]"
                  >
                    <v-list-item-title v-text="sub[0]"></v-list-item-title>
                    <v-list-item-icon>
                    </v-list-item-icon>
                  </v-list-item>
                
              </v-list-group>
        
            </div>
            </v-list>
          </v-navigation-drawer>
          <v-app-bar
            style="background-color: rgba(49, 45, 45, 0.637); z-index:2"
            :clipped-left="clipped"
            fixed
            app
          >
            <v-app-bar-nav-icon @click.stop="drawer = !drawer" />
            <v-toolbar-title v-text="title" />
          </v-app-bar>
          <v-content>
            <v-container>
              <nuxt />
            </v-container>
          </v-content>
          <v-footer
            :fixed="fixed"
            app
          >
            <span>TEST SOUL PARKING &copy; {{ new Date().getFullYear() }}</span>
          </v-footer>
        </v-app>
      </div>
      <!-- <div v-if="!isLogin && $router.history.current.path === '/login'">
        <Nuxt />
      </div> -->
    </div>
  </no-ssr>
</template>

<script>
  export default {
    data () {
      return {
        title: 'SOUL PARKING',
        drawer: false,
        fixed: false,
        clipped: false,
        subItem: [
        ['Petugas Parkir' , '/gaskir'],
      ],
        color: 'primary',
        colors: [
          'primary',
          'blue',
          'success',
          'red',
          'teal',
        ],
        right: true,
        rightdrawer: false,
        miniVariant: false,
      }
    },
    computed: {
      bg () {
        return this.background ? 'https://cdn.vuetifyjs.com/images/backgrounds/bg-2.jpg' : undefined
      },
    },
  }
</script>


<style>

.title {
  font-family:
    'Quicksand',
    'Source Sans Pro',
    -apple-system,
    BlinkMacSystemFont,
    'Segoe UI',
    Roboto,
    'Helvetica Neue',
    Arial,
    sans-serif;
  display: block;
  font-weight: 300;
  font-size: 100px;
  color: #35495e;
  letter-spacing: 1px;
}

.subtitle {
  font-weight: 300;
  font-size: 42px;
  color: #526488;
  word-spacing: 5px;
  padding-bottom: 15px;
}

.links {
  padding-top: 15px;
}
</style>
