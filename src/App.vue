<template>
  <v-app grey darken-4>
    <navbar />
 <v-content  class="mx-4">
   <router-view></router-view>
 </v-content>
  </v-app>
</template>

<script>

import Navbar from './components/navbar'
  export default {
    name: 'App',
      components:{
        Navbar
    },
    data () {
   return{
     //
   }
    },
  
  }
</script>
