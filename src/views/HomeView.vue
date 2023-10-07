<template>
  <div class="home">
    <h1>Homepage</h1>
    <p class="blue white--text">Lorem ipsum dolor sit amet consectetur adipisicing elit. Sequi, repellat perspiciatis
      numquam voluptates debitis nam at iusto ipsum nihil sed omnis odit atque, velit amet. Asperiores debitis in tempora.
      Dolorem.</p>
    <h1 class="display-4 text-uppercase">Massive Text</h1>
    <v-btn depressed color="indigo white--text">Click Here</v-btn>
    <v-btn text color="red">Click Me</v-btn>

    <v-btn depressed>
      <v-icon left>mdi-database</v-icon>
      <span>Backup</span>
    </v-btn>

    <v-btn small>
      <v-icon left small>mdi-database</v-icon>
      <span>Backup</span>
    </v-btn>

    <v-btn large>
      <v-icon left large>mdi-database</v-icon>
      <span>Backup</span>
    </v-btn>

    <v-btn class="mx-2" fab dark small color="pink">
      <v-icon dark>
        mdi-heart
      </v-icon>

      <v-btn large class="hidden-md-and-up">
      <v-icon left large>mdi-database</v-icon>
      <span>Backup</span>
    </v-btn>

    </v-btn>

  </div>
</template>

<script>
export default {
  name: 'HomeView',
}
</script>
