<template>
    <v-app id="inspire">
        <v-app-bar
            app
            color="white"
            flat
        >
            <v-container class="py-0 fill-height">
                <router-link to="/">
                    <v-avatar
                        class="mr-10"
                        color="grey darken-1"
                        size="32"
                    ></v-avatar>
                </router-link>

                <router-link
                    v-for="link in links"
                    :key="link"
                    :to="link.path"
                >
                    <v-btn text>
                        {{ link.name }}
                    </v-btn>
                </router-link>

                <v-spacer></v-spacer>

                <v-responsive max-width="260">
                    <v-text-field
                        dense
                        flat
                        hide-details
                        rounded
                        solo-inverted
                    ></v-text-field>
                </v-responsive>
            </v-container>
        </v-app-bar>

        <v-main class="grey lighten-3">
            <router-view></router-view>
        </v-main>
    </v-app>
</template>

<script lang="ts">
import Vue from 'vue'
import {Component} from "vue-property-decorator";

@Component
export default class App extends Vue{
    public links = [
        {
            name: "About",
            path: "/about",
        },
        {
            name: "Contacts",
            path: "/contacts"
        }
    ];
}
</script>
