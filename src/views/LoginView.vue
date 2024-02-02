<template>
    <v-container>
      
      <v-img src="../assets/logo.png" class="imagem"></v-img>
      <v-row justify="center">

        <v-col cols="12" sm="8" md="6" style="
    margin-top: 16%;
">
          <v-card>
            <v-card-title class="headline">Login</v-card-title>
            <v-card-text>
              <v-form @submit.prevent="login">
                <v-text-field
                  v-model="username"
                  label="Usuário"
                  required
                  outlined
                ></v-text-field>
                <v-text-field
                  v-model="password"
                  label="Senha"
                  type="password"
                  required
                  outlined
                ></v-text-field>
                <router-link to="/home">
                <v-btn class="button" type="submit">Login</v-btn>
              </router-link>
              </v-form>
            </v-card-text>
          </v-card>
        </v-col>
      </v-row>
    </v-container>
  </template>
  
  <script>
  export default {
    name: 'LoginView',

    data() {
      return {
        username: '',
        password: ''
      };
    },
    methods: {
      login() {
        // Aqui você pode adicionar lógica para autenticar o usuário
        // Por exemplo, enviar uma solicitação para o backend
        console.log('Username:', this.username);
        console.log('Password:', this.password);
        
        // Após a autenticação bem-sucedida, você pode redirecionar o usuário para outra página
        // Por exemplo: this.$router.push('/dashboard');
      }
    }
  };
  </script>
  
  <style scoped>
  .v-container {
    margin-top: 50px;
  }
  .imagem{
    width: 20%;
    margin-bottom: -16%;
    left: 40%;
  }
  .button{
    background-color: orange !important;
    color: white !important;
  }
  </style>
  