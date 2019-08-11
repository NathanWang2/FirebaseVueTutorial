<template>
  <v-app>
     <v-navigation-drawer
      v-model="sideNav"
      app
    >

    <v-list-item>
        <v-list-item-content>
          <v-list-item-title class="title">
            Links
          </v-list-item-title>
        </v-list-item-content>
      </v-list-item>

      <v-divider></v-divider>

      <v-list
        nav
      >
        <v-list-item>
          <v-list-item-icon>
            <v-icon>mdi-account-group</v-icon>
          </v-list-item-icon>

          <v-list-item-content>
            <v-list-item-title>View Meetups</v-list-item-title>
          </v-list-item-content>
        </v-list-item>
      </v-list>
    </v-navigation-drawer>

    <v-app-bar
      app
      dark
      class="teal darken-4"
    >
      <v-app-bar-nav-icon @click.stop="sideNav = !sideNav"
      class="hidden-sm-and-up" />
      <v-toolbar flat class="teal darken-4">
        <v-toolbar-title>Dev Meetup</v-toolbar-title>
          <v-spacer></v-spacer>
          <v-toolbar-items class="hidden-xs-only">
            <v-btn text>
              <v-icon left>mdi-account-group</v-icon>
              View Meetups
            </v-btn>
        </v-toolbar-items>
      </v-toolbar>
    </v-app-bar>
     <v-content>
      <v-container
        fluid
        fill-height
      >
        <v-layout>
          <v-flex text-xs>
            <h1>HELLO</h1>
          </v-flex>
        </v-layout>
      </v-container>
    </v-content>
    <!-- Not sure why, but locally it was required to have max height -->
    <!-- <v-toolbar max-height=4em> -->
    <!-- <v-toolbar>
      <v-app-bar-nav-icon @click.stop="sideNav=!sideNav"></v-app-bar-nav-icon>
      <v-toolbar-title>DevMeetUp</v-toolbar-title>

    <v-spacer></v-spacer>
    <v-toolbar-items>
      <v-btn text>
        <v-icon left>mdi-account-group</v-icon>
        Link 1
      </v-btn>
      <v-btn text>Link 2</v-btn>
      <v-btn text>Link 3</v-btn>
    </v-toolbar-items>
  </v-toolbar>
  <v-navigation-drawer v-model="sideNav">
      <v-list>
        <v-list-tile>
          <v-list-tile-action>
            <v-icon left>mdi-account-group</v-icon>
          </v-list-tile-action>
          <v-list-tile-content>View Meetups</v-list-tile-content>
        </v-list-tile>
      </v-list>
    </v-navigation-drawer> -->
    <!-- <h1> OTHER STUFF</h1>
    <main>
      <h1> Random Header </h1>
    </main> -->
  </v-app>
</template>

<script>
export default {
  data: () => {
    return {
      sideNav: false
    }
  }
}
</script>
