<template>
  <span>
    
    <!-- <HelloWorld msg="Welcome to Your Vue.js App"/> -->
    <!-- <hello-world></hello-world> -->
    <home-hero></home-hero>
  </span>
</template>

<script>
// @ is an alias to /src
// import HelloWorld from '@/components/HelloWorld.vue';
import HomeHero from '@/components/HomeHero';

export default {
  name: 'Home',
  components: {
    // HelloWorld
    HomeHero
  }
}
</script>
