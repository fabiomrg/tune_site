<template>
  <v-menu
    v-model="menu"
    :close-on-content-click="true"
    bottom
    left
    max-width="100%"
    min-width="120"
    offset-x
    offset-y
    origin="top left"
    transition="scale-transition"
  >
    <template #activator="{ attrs, on }">
      <v-card
        id="settings"
        class="py-2 px-4"
        flat
        style="position: fixed; top: 16px; left: -5px;"
        width="70"
        v-bind="attrs"
        v-on="on"
      >
        <v-icon large color="black">
          mdi-menu
        </v-icon>
      </v-card>
    </template>

    <v-card class="py-2">
      <br/>
      <base-title
        align="center"
        title="Menu"
        space="0"
      />

      <v-card-text>
    
        <v-divider class="my-6" />
        <base-btn
          block
          @click="$vuetify.goTo('#theme-features')"
          class="mb-6"
          color="black"
          outlined
          target="_blank"
        >
        
        Serviços
        </base-btn>
        <base-btn
          block
          @click="$vuetify.goTo('#features')"
          class="mb-6"
          color="black"
          outlined
          target="_blank"
        >
        
          Tecnologia
        </base-btn>
          
          <base-btn
          block
          @click="$vuetify.goTo('#social')"
         
          class="mb-6"
          color="black"
          outlined
          target="_blank"
        >
          Contato
        </base-btn>
        

        
    
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
