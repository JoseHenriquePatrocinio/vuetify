<template>
    <nav>
        <v-toolbar>
            <v-toolbar-title class="text-uppercase grey--text">
                <span class="font-weight-light">Byte</span>
                <span>Master</span>
            </v-toolbar-title>
            <v-spacer></v-spacer>
            <v-btn text color="grey">
                <span>Sign out</span>
                <v-icon right>mdi-exit-to-app</v-icon>
            </v-btn>
        </v-toolbar>
    </nav>
</template>

<script>
export default {
    name: "NavbarComp"
}
</script>