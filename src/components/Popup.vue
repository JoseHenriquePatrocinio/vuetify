<template>
    <div>
        <v-dialog max-width="600px">
            <template v-slot:activator="{ on, attrs }">
                <v-btn text class="success" v-bind="attrs" v-on="on">
                    Add new project
                </v-btn>
            </template>
            <v-card>
                <v-card-title>
                    Add new project
                </v-card-title>
            </v-card>
        </v-dialog>
    </div>
</template>

<script>
export default {
    name: "PopupComp"
}
</script>