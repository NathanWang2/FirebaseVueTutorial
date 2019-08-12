<template>
  <v-app>
    <v-navigation-drawer v-model="sideNav" app>
      <v-list-item>
        <v-list-item-content>
          <v-list-item-title class="title">Links</v-list-item-title>
        </v-list-item-content>
      </v-list-item>

      <v-divider></v-divider>

      <v-list nav>
        <v-list-item
        v-for="item in menuItem"
        :key="item.title"
        router
        :to="item.link"
        >
          <v-list-item-icon>
            <v-icon>{{item.icon}}</v-icon>
          </v-list-item-icon>

          <v-list-item-content>
            <v-list-item-title>{{item.title}}</v-list-item-title>
          </v-list-item-content>
        </v-list-item>
      </v-list>
    </v-navigation-drawer>

    <v-app-bar app dark class="teal darken-4">
      <v-app-bar-nav-icon @click.stop="sideNav = !sideNav" class="hidden-sm-and-up" />
      <v-toolbar flat class="teal darken-4">
        <v-toolbar-title>
          <router-link to="/" tag="span" style="cursor: pointer">Dev Meetup</router-link>
        </v-toolbar-title>
        <v-spacer></v-spacer>
        <v-toolbar-items class="hidden-xs-only">
          <v-btn text
            v-for="item in menuItem"
            :key="item.title"
            router
            :to="item.link"
            >
            <v-icon left>{{item.icon}}</v-icon>
            {{item.title}}
          </v-btn>
        </v-toolbar-items>
      </v-toolbar>
    </v-app-bar>
    <main>
      <v-content>
        <v-container fluid>
          <router-view></router-view>
        </v-container>
    </v-content>
    </main>
  </v-app>
</template>

<script>
export default {
  data: () => {
    return {
      sideNav: false,
      menuItem: [
        { icon: 'mdi-account-group', title: 'View Meetups', link: '/meetups' },
        { icon: 'mdi-calendar-plus', title: 'Organize Meetup', link: '/meetup/new' },
        { icon: 'mdi-account', title: 'Profile', link: '/profile' },
        { icon: 'mdi-account-plus', title: 'Sign up', link: '/signup' },
        { icon: 'mdi-lock-open', title: 'Sign in', link: '/signin' }
      ]
    }
  }
}
</script>
