<template>
  <v-app>
    <v-navigation-drawer v-model="sideNav" app>
      <v-list-item>
        <v-list-item-content>
          <v-list-item-title class="title">Links</v-list-item-title>
        </v-list-item-content>
      </v-list-item>

      <v-divider></v-divider>

      <v-list nav v-for="item in menuItem" :key="item.title">
        <v-list-item>
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
        <v-toolbar-title>Dev Meetup</v-toolbar-title>
        <v-spacer></v-spacer>
        <v-toolbar-items class="hidden-xs-only" v-for="item in menuItem" :key="item.title">
          <v-btn text>
            <v-icon left>{{item.icon}}</v-icon>
            {{item.title}}
          </v-btn>
        </v-toolbar-items>
      </v-toolbar>
    </v-app-bar>
    <v-content>
      <v-container fluid fill-height>
        <v-layout>
          <v-flex text-xs>
            <h1>HELLO</h1>
          </v-flex>
        </v-layout>
      </v-container>
    </v-content>
  </v-app>
</template>

<script>
export default {
  data: () => {
    return {
      sideNav: false,
      menuItem: [
        { icon: 'mdi-account-group', title: 'View Meetups' },
        { icon: 'mdi-account', title: 'Profile' },
        { icon: 'mdi-calendar-plus', title: 'Organize Meetup' },
        { icon: 'mdi-account-plus', title: 'Sign up' },
        { icon: 'mdi-lock-open', title: 'Sign in' }
      ]
    }
  }
}
</script>
