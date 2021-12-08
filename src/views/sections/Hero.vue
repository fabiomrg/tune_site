<template>
  <section id="hero">
    
    <v-img
      :min-height="minHeight"
      :src="require('@/assets/vendas_bg.jpg')"
      class="white--text"
      gradient="to bottom, rgba(11, 28, 61, .9), rgba(0,0,0,.5)"
    >
      <v-container class="fill-height px-4 py-12">
        <v-responsive
          class="d-flex align-center mx-auto"
          height="100%"
          max-width="700"
          width="100%"
        >
          <base-subheading
            weight="regular"
            title="CRIANDO SOLUÇÕES PARA SUA LOJA OU NEGÓCIO"
          />

           <base-heading
             size="text-h2"
            title="..RÁPIDO E FÁCIL!"
            weight="medium"
          />

          <base-body>
            Entre em contato diretamente com nossa equipe. Sabemos o quão complexo é empreender e todo tempo é valioso, por isso conseguiremos te ajudar de forma otimizada e com todo o necessário para seu negócio ser representado digitalmente. 
          </base-body>

          <div
            :class="$vuetify.breakpoint.smAndDown ? 'flex-column align-start' : 'align-center'"
            class="d-flex flex-wrap"
          >
            <base-btn @click="$vuetify.goTo('#theme-features')">
              Veja as possibilidades
            </base-btn>
 <br/> <br/> <br/> <br/>
          </div>
        </v-responsive>
      </v-container>
    </v-img>
  </section>
</template>

<script>
  export default {
    name: 'SectionHero',

    provide: {
      theme: { isDark: true },
    },

    computed: {
      minHeight () {
        const height = this.$vuetify.breakpoint.mdAndUp ? '100vh' : '50vh'

        return `calc(${height} - ${this.$vuetify.application.top}px)`
      },
    },
  }
</script>
