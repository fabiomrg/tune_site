<template>
  <v-theme-provider dark>
    <base-section
      id="social"
      class="accent text-center"
      space="56"
    >
      <base-icon class="mb-8">
        mdi-card-account-phone
      </base-icon>

      <base-section-heading
        color="transparent"
        title="Contato"
      >
        Será um prazer poder ajudá-lo! Estamos aguardando seu contato:
      </base-section-heading>
        
        <v-icon right>
          mdi-whatsapp
        </v-icon>
        (11) 93375-2843 <br/><br/>
        <v-icon left>
            mdi-mail
          </v-icon>
          contato@tunewest.com
          <br/><br/>
      <div class="py-4" />

      <v-btn
        class="font-weight-bold"
        color="white"
        href="https://api.whatsapp.com/send/?phone=5511933752843&text=Olá! Preciso de ajuda para meu negócio."
        light
        min-width="168"
        target="_blank"
        x-large
      >
        Toque aqui para whatsapp

        <v-icon right>
          mdi-whatsapp
        </v-icon>
      </v-btn>
    </base-section>
  </v-theme-provider>
</template>

<script>
  export default {
    name: 'SectionNews',

    provide: {
      heading: { align: 'center' },
    },
  }
</script>
