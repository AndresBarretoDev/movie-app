<template>
    <div>
        <!-- SIDEBAR MOBILE -->
        <v-navigation-drawer v-if="drawer" app absolute dark disable-resize-watcher class="deep-purple" v-model="drawer" >
            <v-list>
                <v-list-item v-for="(item,indexm) in menuBar" :key="indexm" link>
                    <v-list-item-icon>
                        <v-icon>{{item.icon}}</v-icon>
                    </v-list-item-icon>

                    <v-list-item-content>
                        <v-list-item-title>
                            <router-link v-bind:to="item.url" class="item.class">{{item.name}}</router-link>
                        </v-list-item-title>
                    </v-list-item-content>
                </v-list-item>
            </v-list>
        </v-navigation-drawer>
        <!-- SIDEBAR MOBILE -->
        <!-- NAVIGATION BAR -->
        <v-toolbar relative color="#fff" class="toolbar">
            <div class="toolbar__container">
                <div class="toolbar__logo">
                    <router-link to="/" class="toolbar__logo__box">
                        <img src="@/assets/images/logo.png" alt="logo movies app" class="toolbar__img" />
                    </router-link>
                </div>
                <div class="toolbar__nav">
                    <ul class="toolbar__list">
                        <li class="toolbar__list__item" v-for="(item, index) in menuBar" :key="index">
                            <router-link v-bind:to="item.url" class="opSemBold ttU">{{item.name}}</router-link>
                        </li>
                    </ul>
                </div>
                <v-app-bar-nav-icon  class="toolbar__burger" @click="drawer = !drawer"></v-app-bar-nav-icon>
            </div>

        </v-toolbar>
    </div>
</template>

<script>
    // @ is an alias to /src

    export default {
        name: 'navigation',
        components: {
            
        },
        data() {
            return {
                drawer: false,
                menuBar: [{
                        id: 1,
                        name: "home",
                        url: "/",
                        icon: 'mdi-view-dashboard'
                    },
                    {
                        id: 2,
                        name: "categories",
                        url: "/categories",
                        icon: 'mdi-view-dashboard'
                    },
                    {
                        id: 3,
                        name: "my favorites",
                        url: "/my-favorites",
                        icon: 'mdi-view-dashboard'
                    },
                    {
                        id: 4,
                        name: "sign in",
                        url: "/signin",
                        icon: 'mdi-view-dashboard'
                    }
                ]
            }
        },
    }
</script>