<template>
  <div>
    <v-app-bar
      id="home-app-bar"
      app
      elevation="1"
      elevate-on-scroll
      height="80"
    >
    <v-row no-gutters justify="center">
      <home-menu/>
      <v-spacer />
      <base-img
        :src="require('@/assets/testelogo2.svg')"
        class="mr-3"
        contain
        max-width="60"
        width="100%"
      />
    </v-row>
      <base-img
        :src="require(`@/assets/tune-logo-${$vuetify.theme.isDark ? 'dark' : 'light'}.svg`)"
        contain
        max-width="70"
        width="100%"
      />

      <v-spacer />


     

     
    </v-app-bar>
  </div>
</template>

<script>
  export default {
    name: 'HomeAppBar',

    data: () => ({
      drawer: null,
      items: [
        'Home',
        'Pro',
      ],
    }),
    components: {
      
      HomeMenu: () => import('@/layouts/home/menu'),
    },
  }
</script>

<style lang="sass">
  #home-app-bar
    .v-tabs-slider
      max-width: 24px
      margin: 0 auto

    .v-tab
      &::before
        display: none
</style>
