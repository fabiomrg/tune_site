<template>
  <v-menu
    v-model="menu"
    :close-on-content-click="true"
    bottom
    left
    max-width="100%"
    min-width="320"
    offset-x
    offset-y
    origin="top right"
    transition="scale-transition"
  >
    <template #activator="{ attrs, on }">
      <v-card
        id="settings"
        class="py-2 px-4"
        color="#0000004D"
        dark
        flat
        style="position: fixed; top: 80px; right: -35px;"
        width="100"
        v-bind="attrs"
        v-on="on"
      >
        <v-icon large>
          mdi-whatsapp
        </v-icon>
      </v-card>
    </template>

    <v-card class="py-2">
     
      <v-card-text>

        <base-btn
          block
          href="https://api.whatsapp.com/send/?phone=5511933752843&text=Olá! Estou precisando de ajuda para meu negócio."
          class="mb-6"
          color="black"
          outlined
          target="_blank"
        >
        <v-icon left>
            mdi-whatsapp
          </v-icon>
          Toque aqui para Whatsapp
        </base-btn>
          <div
          class="mr-4"
         
        >
        <div
          class="mr-4"
         
        >
          <v-icon left>
            mdi-phone
          </v-icon>
          (11)93375-2843
        </div>
         <v-divider class="my-6" />
          <v-icon left>
            mdi-mail
          </v-icon>
          contato@tunewest.com
        </div>

       
      
      </v-card-text>
    </v-card>
  </v-menu>
</template>

<script>
  export default {
    name: 'HomeSettings',

    data () {
      return {
        colors: [
          this.$vuetify.theme.currentTheme.primary,
          '#9368e9',
          '#F4511E',
        ],
        menu: false,
      }
    },

    computed: {
      currentThemePrimary: {
        get () {
          return this.$vuetify.theme.currentTheme.primary
        },
        set (val) {
          const target = this.$vuetify.theme.isDark ? 'dark' : 'light'

          this.$vuetify.theme.themes[target].primary = val
        },
      },
    },
  }
</script>
