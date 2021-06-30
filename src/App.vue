<template>
  <v-app>

    <v-main>
      <hero />

      <about-me />

      <skills />

      <!-- <experience /> -->

      <portfolio />

      <!-- <contact /> -->
    </v-main>
  </v-app>
</template>

<script>
export default {
  name: 'App',

  components: {
    Hero: () => import('./components/Hero'),
    AboutMe: () => import('./components/AboutMe'),
    Skills: () => import('./components/Skills'),
    // Experience: () => import('./components/Experience'),
    Portfolio: () => import('./components/Portfolio'),
    // Contact: () => import('./components/Contact'),
  },

  data: () => ({
    //
  }),
};
</script>
