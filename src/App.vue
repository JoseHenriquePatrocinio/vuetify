<template>
  <v-app>
    <NavbarComp />
    <v-main class="mx-4 mb-4">
      <router-view />
    </v-main>
  </v-app>
</template>

<script>
import NavbarComp from '@/components/NavbarComp.vue'
export default {
  name: 'App',
  components: {
    NavbarComp
  },
  data: () => ({

  }),
};
</script>
