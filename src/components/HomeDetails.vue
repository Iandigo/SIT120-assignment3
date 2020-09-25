<template>
  <v-content>
    <!-- About -->
    <div class="staticHero">
      <v-img src="../assets/images/img13.jpg">
        <v-row align="end" class="lightbox white--text pa-2 fill-height">
          <v-col>
            <v-container>
              <div class="headline">About Us</div>
            </v-container>
          </v-col>
        </v-row>
      </v-img>
    </div>
    <div class="block">
      <v-container>
        <p>Photolipho is a online photo management and sharing application to all around the world. We want to help people make their photos available to the people who matter to them. We also want to enable new ways of organizing photos and video. Photolipho continues to evolve in myriad ways, all of which are designed to make it easier and better. Join our comunity for free and enjoy your journey!</p>
      </v-container>
    </div>
    <div class="block">
      <v-container>
        <h2 class="text-center">Our Teams</h2>
        
            <v-card flat tile class="mx-16">
              <v-img :src="src" aspect-ratio="3" class="grey lighten-2"></v-img>
              <v-card-text class="text--primary text-center">
                <div class="title">{{name }}</div>
                <p>{{title }}</p>
              </v-card-text>
            </v-card>
          
      </v-container>
    </div>
  </v-content>
</template>

<script>
export default {
  name: "HomeDetails",
  data() {
    return {
      src: require("../assets/images/me.jpeg"),
      name: 'Ian Nguyen',
      title: 'Developer'
    };
  }
};
</script>