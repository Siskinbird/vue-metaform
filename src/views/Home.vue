<!-- <template>
  <div class="home">
    <section class="hero">
      <div class="hero-text container">
          <h4>Just text for hero section</h4>
          <hr />
          <h2>Whith my try</h2>
          <hr />
          </div>
          <VideoBack></VideoBack>
      </section>
    </div>
  </template> -->
  <script>
// @ is an alias to /src
import Navigation from '@/components/Navigation.vue'
import VideoBack from '@/components/VideoBack.vue'

export default {
  name: 'Home',
  components: {
    Navigation
}
}
</script>
<style lang="scss" scoped>
  .hero-text {
    background-color: #fff;
  }
</style>
