<template>
  <div class="app">
    <Navigation />
    <VideoBack />
    <About />
    <Services />
    <FeedbackForm />
    <Footer> </Footer>
    </div>
</template>

<script>
  import Navigation from './components/Navigation.vue';
  import VideoBack from './components/VideoBack.vue';
  import About from './components/About.vue';
  import Services from './components/Services.vue';
  import FeedbackForm from './components/FeedbackForm.vue';
  import Footer from './components/Footer.vue';
  export default {
    name: "App",
    components: { 
      Navigation,
      VideoBack,
      About,
      Services,
      FeedbackForm,
      Footer
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

@mixin phone-xs {
  @media (max-width: 360px) { @content; }
}
@mixin for-phone-only {
  @media (max-width: 599px) { @content; }
}
@mixin tablet-portrait {
  @media (min-width: 600px) { @content; }
}
@mixin tablet {
  @media (min-width: 900px) { @content; }
}
@mixin desktop {
  @media (min-width: 1200px) { @content; }
}
@mixin xxl {
  @media (max-width: 1800px) { @content; }
}

</style>
