<template>
  <div class="app">
    <Navigation />
    <VideoBack />
    <router-view/>
    </div>
</template>

<script>
  import Navigation from './components/Navigation.vue';
   import VideoBack from './components/VideoBack.vue';
  export default {
    name: "App",
    components: { 
      Navigation,
      VideoBack
    }
};
</script>

<style lang="scss">
@import url("https://fonts.googleapis.com/css2?family=Montserrat:wght@400;500;600;700&display=swap");

* {
  padding: 0;
  margin: 0;
  box-sizing: border-box;
  font-family: 'Montserrat', sans-serif;
  font-weight: 400;
}

.app {
  min-height: 100vh;
  position: relative;
  background-color: #fff;
}

.container {
  padding: 0 20px;
  max-width: 1140px;
  margin: 0 auto;
}

</style>
