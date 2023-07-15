<template>
  <v-app>
    <default-bar />
      <ban/> 
      <carrousel/>
      <emerg/>
    <default-view />
    <footerView/>
  </v-app>
</template>

<script setup>
  import DefaultBar from './AppBar.vue'
  import DefaultView from './View.vue'
  import ban from '../components/hello.vue'
  import carrousel from '../components/carrousel.vue'
  import emerg from '../components/emerg.vue'
  import footerView from './footer.vue'
</script>
