<template>
    <v-footer>
    <v-col cols="1" align-self="center">
      <v-img src="../assets/logo.png"
      max-width="100"
      max-height="150"> </v-img>
    </v-col>
    <v-container>
      <v-layout justify-center>
        <v-flex>
          <v-card flat>
            <v-card-text class="text-center">
              © 2023. Todos los derechos reservados.
              
            </v-card-text>
          </v-card>
        </v-flex>
      </v-layout>
    </v-container>
  </v-footer>
</template>

<script>
   export default{
        name: 'footerView',
        data(){

        }
    }
</script>