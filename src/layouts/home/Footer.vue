<template>
  <v-footer
    id="home-footer"
    color="black"
    dark
    min-height="72"
  >
    <v-container>
      <v-row>
        

        <v-col
          class="text-center"
          cols="12"
          
        >
          Copyright &copy; {{ new Date().getFullYear() }} TuneWest
        </v-col>
      </v-row>
    </v-container>
  </v-footer>
</template>

<script>
  export default {
    name: 'HomeFooter',

    data: () => ({
      social: [
       
      ],
    }),
  }
</script>

<style lang="sass">
  #home-footer a
    text-decoration: none
</style>
