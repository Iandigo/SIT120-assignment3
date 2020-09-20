<template>
  <v-app>
     <header>
       <Navbar/> 
     </header>
     
    <router-view/>

    <v-footer>
        <Footer />
    </v-footer>
    
  </v-app>
</template>

<script>
import Navbar from './components/Navbar';
import Footer from "./components/Footer";
export default {
  name: 'App',

  components: {
    Navbar,
    Footer
  },

  data: () => ({
    //
  }),
};
</script>
<style>
</style>