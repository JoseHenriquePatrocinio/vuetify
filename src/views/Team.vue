<template>
  <div class="team">
    <h1 class="text-subtitle-1 grey--text">This is the team page</h1>

    <v-container class="my-5">

      <v-layout row wrap>
        <v-flex xs12 sm6 md4 lg3 v-for="person in team" :key="person.name">
          <v-card text class="text-xs-center ma-3">
            <v-responsive class="pt-4 text-center">
              <v-avatar size="100" class="grey lighten-2">
                <img :src="person.avatar">
              </v-avatar>
            </v-responsive>
            <v-card-text>
              <div class="subheading text-center">{{ person.name }}</div>
              <div class="grey--text text-center">{{ person.role }}</div>
            </v-card-text>
            <v-card-actions>
              <v-btn text color="grey">
                <v-icon small left>mdi-message</v-icon>
                <span>Message</span>
              </v-btn>
            </v-card-actions>
          </v-card>
        </v-flex>
      </v-layout>
    </v-container>
  </div>
</template>
  
<script>
export default {
  name: 'TeamView',
  data() {
    return {
      team: [
        { name: 'The Net Ninja', role: 'Web developer',avatar:'/avatar-1.png' },
        { name: 'Ryu', role: 'Graphic designer',avatar:'/avatar-2.png' },
        { name: 'Chun Li', role: 'Web developer',avatar:'/avatar-3.png' },
        { name: 'Gouken', role: 'Social media maverick',avatar:'/avatar-4.png' },
        { name: 'Yoshi', role: 'Sales guru',avatar:'/avatar-5.png' }
      ]
    }
  }
}
</script>