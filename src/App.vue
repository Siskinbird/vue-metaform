<template>
  <div class="app">
    <Navigation />
    <router-view/>
    </div>
</template>

<script>
  import Navigation from './components/Navigation.vue';
  export default {
    name: "App",
    components: { Navigation }
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

.container {
  padding: 0 20px;
  max-width: 1140px;
  margin: 0 auto;
}

.app {
  font-family: Montserrat, Helvetica, Arial, sans-serif;
  -webkit-font-smoothing: antialiased;
  -moz-osx-font-smoothing: grayscale;
  text-align: center;
  color: #2c3e50;
}

</style>
