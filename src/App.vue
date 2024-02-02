<template>
  <v-app>
    <v-app-bar
      app
      color="#Ff8600"
      
        class="barra"
    >
      <div class="d-flex align-center">
    

        <v-img
          alt="Vuetify Name"
          contain
          min-width="70"
         
          src="../src/assets/logo.png"
         
          width="10"
          class="imagem"
        />
        <h2 style="color: white;position: relative;margin-left: -22%; left: 21%;" > Tech Burguer</h2>
      </div>

      <v-spacer></v-spacer>

    
    </v-app-bar>

    <v-main>
      <router-view/>
    </v-main>
  </v-app>
</template>

<script>

export default {
  name: 'App',

  data: () => ({
    //
  }),
};
</script>
<style scoped>

.barra{
  left: 0px !important; 
  
}
.imagem{
  margin-left: 22% !important;
}
</style>
