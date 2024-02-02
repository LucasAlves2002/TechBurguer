<template>
  <v-sheet class="mx-auto" elevation="8" max-width="800">
    <v-slide-group v-model="model" class="pa-4" show-arrows>
      <v-slide-item v-for="(image, index) in images" :key="index" v-slot="{ active, toggle }">
        <v-card :color="active ? 'primary' : 'grey lighten-1'" class="ma-4" height="200" width="150" @click="toggle">
          <v-img :src="image.url" height="100%" width="100%" @click.stop="toggle"></v-img>
          <v-row class="fill-height" align="center" justify="center">
            <v-scale-transition>
              <v-icon v-if="active" color="white" size="48" v-text="'mdi-close-circle-outline'"></v-icon>
            </v-scale-transition>
          </v-row>
        </v-card>
      </v-slide-item>
    </v-slide-group>

    <v-expand-transition>
      <v-sheet v-if="model !== null" height="200" tile>
        <v-row class="fill-height" align="center" justify="center">
          <h3 class="text-h7" style="
    width: 90%;
">
             {{ selectedText }}
          </h3>
          <v-btn class="button"> <v-icon left>
            mdi-cart-outline
          </v-icon>Comprar</v-btn>
        </v-row>
      </v-sheet>
    </v-expand-transition>
  </v-sheet>

</template>

<script>
export default {
  name: 'SliderView',
  data() {
    return {
      model: null,
      images: [
        { url: require('@/assets/hamburguer0.jpg'), text: "Queijo Deluxe Burger é uma combinação deliciosa de pão tostado, carne suculenta e queijo derretido. A carne é coberta com queijo, que derrete e adiciona um sabor cremoso. Geralmente acompanhado de alface, tomate, cebola e molhos, oferecendo uma explosão de sabores. É uma opção clássica e satisfatória, perfeita para os amantes de hambúrgueres." },
        { url: require('@/assets/hamburguer1.jpg'), text: "Duplo Sabor Burger uma opção substancial e suculenta, composta por dois generosos discos de carne grelhada, proporcionando uma experiência intensa de sabor e textura. Geralmente acompanhado por queijo derretido, alface fresca, tomate e uma variedade de molhos, entre outros complementos, é uma escolha popular para quem deseja uma refeição satisfatória e reconfortante." },
        { url: require('@/assets/hamburguer2.jpg'), text: "O Baconator Burger é uma explosão de sabores para os amantes de bacon. Com um disco suculento de carne grelhada, é coberto com bacon crocante, queijo derretido, alface, tomate e cebola caramelizada. Servido entre dois pães tostados, é uma indulgência deliciosa e satisfatória." },
        { url: require('@/assets/hamburguer3.jpg'), text: "O Supremo X-Tudo é um hambúrguer completo e delicioso, ideal para quem busca uma explosão de sabores. Com um suculento disco de carne grelhada, é recheado com bacon crocante, queijo derretido, alface fresca, tomate maduro, cebola caramelizada e picles. Servido entre dois pães tostados, este hambúrguer oferece uma experiência gastronômica satisfatória e memorável." },
        { url: require('@/assets/hamburguer4.jpg'), text: "O Nugget Supreme Burger é uma criação única para os amantes de nuggets de frango. Este hambúrguer apresenta uma base de suculento hambúrguer de frango empanado, inspirado nos saborosos nuggets de frango crocantes. Cada mordida oferece uma explosão de sabor, combinando a textura crocante dos nuggets com a suculência do hambúrguer." },
        // Adicione mais URLs de imagens conforme necessário
      ],
    };
  },
  computed: {
    selectedText() {
      if (this.model !== null) {
        return this.images[this.model].text;
      }
      return '';
    },
  },
};
</script>
<style scoped>
.button{
    background-color: orange !important;
    color: white !important;
  }
</style>
