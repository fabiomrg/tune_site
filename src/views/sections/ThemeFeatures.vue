<template>
  <base-section id="theme-features">
    <base-section-heading  title="Serviços">
     
    </base-section-heading>

    <v-container>
      <v-row>
        <v-col
          v-for="(feature, i) in features"
          :key="i"
          cols="12"
          md="6"
        >
          <base-avatar-card
            v-bind="feature"
            align="left"
            horizontal
          >
            {{feature.text}}
            
          </base-avatar-card>
        </v-col>
      </v-row>
    </v-container>
  </base-section>
</template>

<script>
  export default {
    name: 'SectionThemeFeatures',

    data: () => ({
      features: [
        {
          title: 'Consultoria',
          icon: 'mdi-checkbox-multiple-marked-outline',
          text: 'Como a tecnologia pode ajudar o seu negócio? Migrar os serviços atuais, site dedicado, app ou apenas uma página simples com logo e links importantes? Misturar um pouco de tudo? Devo me preocupar com servidores, publicação? Ajudaremos com essas e muitas outras questões.',
        },
        {
          title: 'Site Rápido',
          icon: 'mdi-web-box',
          text: 'Colocaremos seu site no ar de forma ultra-rápida. Escolha entre 3 opções e pronto! Todos nossos sites e apps são responsivos, funcionam perfeitamente em celular, tablet, computadores.',
        },
        {
          title: 'Site sob medida',
          icon: 'mdi-web',
          text: 'Do seu jeito, com seus detalhes. Escolha entre nossos modelos e peça os ajustes que quiser.',
        },
        {
          title: 'Logo Rápida',
          icon: 'mdi-camera-timer',
          text: 'Criamos sua logo de forma rápida, em até 12h. Enviaremos 5 opções baseadas no segmento do seu negócio. Após a escolha receberá os arquivos e os direitos autorais.',
        },
        {
          title: 'Logo sob medida',
          icon: 'mdi-pencil-box-outline',
          text: 'Logotipo, logomarca, cores...Tudo feito de forma exclusiva e personalizada.',
        },
        {
          title: 'Web app',
          icon: 'mdi-cellphone-text',
          text: 'Precisando de mais "força"? Mandar notificações para clientes? Gostaria de ter um aplicativo com funções mais específicas como: formulários, cadastros, catálogos de produtos. Podemos te ajudar desenvolvendo um web app!',
        },
        {
          title: 'fidelidade digital',
          icon: 'mdi-account-star',
          text: 'O cartão fidelidade digital e personalizado. Com nosso programa de fidelidade conseguimos construir uma base de clientes e fidelizá-los com prêmios: "A cada 10 compras ganhe 1". Seus clientes se sentindo especiais e próximos' ,
        },
        {
          title: 'Cardápio digital',
          icon: 'mdi-qrcode-scan',
          text: 'Coloque o QR Code na mesa, balcão e onde mais for necessário. Seu cardápio, produtos, serviços com fácil acesso para os clientes.' ,
        },

        {
          title: 'vendas online',
          icon: 'mdi-cart',
          text: 'Integramos seu site com o catálogo do whatsapp. Também criamos seu próprio catálogo personalizado. Precisando vender e receber pela internet utilizando cartão de credito? Fazemos também!' ,
        },
      ],
    }),
  }
</script>
