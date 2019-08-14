<template>
    <v-container>
        <v-layout row wrap>
            <v-flex xs12 sm6 class="text-sm-right">
                <v-btn
                    large
                    router
                    to="/meetups"
                    class="primary">Explore Meetups</v-btn>
            </v-flex>
             <v-flex xs12 sm6 class="text-sm-left">
                <v-btn
                    large
                    router
                    to="/meetups"
                    class="primary">Organize Meetup</v-btn>
            </v-flex>
        </v-layout>
    </v-container>
</template>
