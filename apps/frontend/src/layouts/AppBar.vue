<template>
  <v-app-bar flat color="#f5fcfc" height="120px">
    <v-app-bar-title>
      <v-img cover src="src\assets\logob.png" width="100" height="108"></v-img>
    </v-app-bar-title>
    <v-spacer></v-spacer>
    <v-btn text v-for="item in menu" :key="item.icon" :to="item.path" :color="item.color" :class="{'blue-button': item.path === '/donations'}">
      <v-icon :icon="item.icon" start></v-icon>
      {{item.text}}
    </v-btn>
    <v-spacer />
    <v-btn text v-if="userNeedLogin">
      <v-icon icon="mdi-login" start></v-icon>
      Iniciar Sesión
    </v-btn>
    <v-btn text v-else>
      <v-icon icon="mdi-logout" start></v-icon>
      Cerrar Sesión
    </v-btn>
    <v-btn text to="/login">
      <v-icon icon="mdi-account-plus" start></v-icon>
      Registrarse
    </v-btn>
  </v-app-bar>
</template>

<style>
.blue-button {
  background-color: red !important;
  color: white !important;
}
</style>

<script>
  export default{
    name: 'AppBar',
    data(){
      return{
        userNeedLogin: false,
        menu: [
          {
            path: '/home',
            icon: 'mdi-home',
            text: 'Inicio',
            color: 'red'
          },
          {
            path: '/contact',
            icon: 'mdi-card-account-mail',
            text: 'Contacto',
            color: 'red'
          },
          {
            path: '/history',
            icon: 'mdi-file-document',
            text: 'Historia',
            color: 'red'
          },
          {
            path: '/donations',
            icon: 'mdi-hand-heart-outline',
            text: 'Donaciones',
            
          }
          
        ]
      }
    }
  }
</script>
