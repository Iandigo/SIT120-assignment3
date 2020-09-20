<template>
    <v-card
      color="grey lighten-4"
      flat
      height="45px"
      tile
    >
      <v-toolbar dense color="BLACK" dark>
        <Dropdown/>
  
        <v-toolbar-title>Photolipho</v-toolbar-title>
  
        <v-spacer></v-spacer>
        <v-toolbar-items class="hidden-sm-and-down">
          
          <v-btn flat to="/signup">
            Sign Up
          </v-btn>
    
          <v-btn flat to="/login">
            Log In
          </v-btn>
        </v-toolbar-items>
      </v-toolbar>
    </v-card>
</template>

<script>
import Dropdown from './Dropdown';
export default {
    name: 'navbar',
     components: {
         Dropdown
    
  },

  data() {
    return {
     
    }
  },
}
</script>