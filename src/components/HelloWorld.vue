<template>
  <v-container>
    <v-row class="text-center">
      <v-col cols="12">
        <v-img
          :src="require('../assets/logo.png')"
          class="my-3"
          contain
          height="200"
        />
      </v-col>

      <v-col class="mb-4">
        <h1 class="display-2 font-weight-bold mb-3">
          Welcome to Photolipho
        </h1>

        <p class="subheading font-weight-regular">
          Join our community and enjoy beautifull sceneries around us
          <br>Please sign in for more information
        </p>
      </v-col>
    </v-row>
  </v-container>
</template>

<script>
  export default {
    name: 'HelloWorld',
  }
</script>

<style scoped>
.hello-world{
  background: url("logo.png");
  background-size: cover;
  width: 100%;
  height: 100%;
}
h1{
  color: #D500F9;
}

p{
  color: #D500F9;
}
</style>