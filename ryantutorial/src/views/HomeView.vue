<template>
  <div>
    <h1>Welcome to the wild, no heroes and villains </h1>
    <!-- <cardComp/> -->
   <Manga/>
    <footerComp/>
  </div>
</template>

<script>
  import footerComp from '../components/Footer';
  import Manga from '../components/Manga.vue'
  export default {
    components: {
      footerComp,
      Manga
      
    }
  }
</script>

<style scoped>

</style>