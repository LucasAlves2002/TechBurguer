<template>
    <nav>
      <v-navigation-drawer
          
          app
          dark
          color="rgb(255, 134, 0)"
            permanent
            expand-on-hover
        >
                <v-list>
         
        
             
            
    
              <v-list-item link>
                <v-list-item-content>
                  <v-list-item-title class="text-h6">
                    Menu Burguer
                  </v-list-item-title>
                </v-list-item-content>
              </v-list-item>
            </v-list>
    
            <v-divider></v-divider>
    
            <v-list
              nav
              dense
            >
            <v-list-item link>
            <v-list-item-icon>
                     <v-icon>mdi-phone</v-icon>
            </v-list-item-icon>
        <v-list-item-title style="color: white;">(31) 9 8973-8409</v-list-item-title>
          </v-list-item>  
          <v-list-item link>
            <v-list-item-icon>
                     <v-icon>mdi-whatsapp</v-icon>
            </v-list-item-icon>
        <v-list-item-title style="color: white;">(31) 9 8973-8409</v-list-item-title>
          </v-list-item>  
            </v-list>
            
            
            <template v-slot:append>
            <div class="pa-2">
                <router-link to="/">
              <v-btn block  color="blue" @click="logout" class="button">
                 <v-icon left>
            mdi-logout
          </v-icon>
                Logout
              </v-btn>
            </router-link>
            </div>
          </template>
        </v-navigation-drawer>
        
    </nav>
    </template>
    
    <script>
    export default {
      name: "SideBar",
      data: () => ({
     
        error: false,
      }),
      methods: {
    
        async logout() {
             try {
            this.error = false;
    
              localStorage.removeItem( "jwt");
              this.$router.push("/");
          
            // console.log(res.data.dados[0]);
          } catch (e) {
           window.alert('Não deu!')
          }
        },
      }
    }
      
    </script>
    
    <style scoped>
    .button{
        background-color: #232323 !important;
    color: white !important;
    }
    </style>