<template>
  <div class="home">
    <section class="hero">
      <div class="hero-text container">
          <h4>Just text for hero section</h4>
          <hr />
          <h2>Whith my try</h2>
          <hr />
          </div>
          <img alt="Metaform ico" src="../assets/logo/metaform.png">
         <!--  <HelloWorld msg="Welcome to Your Vue.js App"/> -->
          <!-- <VideoBack></VideoBack> -->
      </section>
    </div>
  </template>
  <script>
// @ is an alias to /src
import Navigation from '@/components/Navigation.vue'
import VideoBack from '@/components/VideoBack.vue'

export default {
  name: 'Home',
  components: {
    Navigation,
    VideoBack
}
}
</script>
<style lang="scss" scoped>
  .hero {
    background-color: #fff;
  }
</style>
