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
                <v-card-text>
                    <v-form class="px-3" ref="form">
                        <v-text-field label="Title" v-model="title" prepend-icon="mdi-folder"
                            :rules="inputRules"></v-text-field>
                        <v-textarea label="Information" v-model="content" prepend-icon="mdi-edit" :rules="inputRules"></v-textarea>

                        <v-menu>
                            <template v-slot:activator="{ on, attrs }">
                                <v-text-field v-model="due" label="Due date" prepend-icon="mdi-calendar" v-bind="attrs"
                                    v-on="on" :rules="inputRules"></v-text-field>
                            </template>
                            <v-date-picker v-model="due" @input="menu = false"></v-date-picker>
                        </v-menu>

                        <v-btn text class="success mx-0 mt-3" @click="submit">Add project</v-btn>
                    </v-form>
                </v-card-text>
            </v-card>
        </v-dialog>
    </div>
</template>

<script>
export default {
    name: "PopupComp",
    data() {
        return {
            title: "",
            content: "",
            due: "",
            menu: false,
            inputRules:[
                v => v.length >= 3 || 'Minimum length is 3 characters'
            ]
        }
    },
    methods: {
        submit() {
            if(this.$refs.form.validate()){
                console.log(this.title, this.content)
            }
        }
    }
}
</script>