<template>
  <base-section
    id="features"
    class="secondary"
  >
   
    <v-responsive
      class="mx-auto"
      max-width="1350"
    >
    <div class="white--text text-darken-1 mb-2">
      <base-section-heading title="Tecnologia"/> 
   
    </div>

      <v-container fluid>
        
        <v-row>
          <v-col
            v-for="card in cards"
            :key="card.title"
            cols="12"
            sm="4"
            md="3"
          >
            <base-info-card
              align="center"
              dark
              v-bind="card"
            />
          </v-col>
        </v-row>
      </v-container>
    </v-responsive>
  </base-section>
</template>

<script>
  export default {
    name: 'SectionFeatures',

    data: () => ({
      cards: [
    
        {
          icon: 'mdi-overscan',
          title: 'Responsivo',
          text: 'Utilizamos tecnologias que nos permite construir sites e aplicações responsivas, que funcionam perfeitamente em todos os tamanhos de tela. Com design moderno, atual e com ótima experiência para o usuário.', 
        },
        {
          icon: 'mdi-cloud-lock-outline',
          title: 'Cloud Compulting',
          text: 'Servidores na nuvem, podendo ser aumentada a capacidade a qualquer momento. Garantia de disponibilidade e segurança.',
        },
      
        {
          icon: 'mdi-archive-search-outline',
          title: 'Otimização SEO',
          text: 'Trabalhamos com padronização dos buscadores do Google, garantindo bom ranqueamento resultados nas buscas',
        },
        {
          icon: 'mdi-puzzle-outline',
          title: 'Suporte',
          text: 'Não se sinta sozinho, estamos perto de você! Atendemos via whatsapp, video chamada e presencial (grande São Paulo).',
        },
      ],
    }),
  }
</script>
