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
                    <v-form class="px-3">
                        <v-text-field label="Title" v-model="title" prepend-icon="mdi-folder"></v-text-field>
                        <v-textarea label="Information" v-model="content" prepend-icon="mdi-edit"></v-textarea>
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
    data(){
        return{
            title:"",
            content:""
        }
    },
    methods:{
        submit(){
            console.log(this.title, this.content)
        }
    }
}
</script>