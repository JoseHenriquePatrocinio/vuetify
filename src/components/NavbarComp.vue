<template>
    <nav>
        <v-app-bar flat app>
            <v-app-bar-nav-icon class="grey--text" @click="drawer = !drawer"></v-app-bar-nav-icon>
            <v-toolbar-title class="text-uppercase grey--text">
                <span class="font-weight-light">Byte</span>
                <span>Master</span>
            </v-toolbar-title>
            <v-spacer></v-spacer>
            <v-btn text color="grey">
                <span>Sign out</span>
                <v-icon right>mdi-exit-to-app</v-icon>
            </v-btn>
        </v-app-bar>

        <v-navigation-drawer app v-model="drawer" class="indigo">

        </v-navigation-drawer>

    </nav>
</template>

<script>
export default {
    name: "NavbarComp",
    data() {
        return {
            drawer: false
        }
    }
}
</script>