<template>
  <section class="contacts">
      <h2>Адрес склада</h2>
      <div id="map" class="map">
        <iframe src="https://yandex.ru/map-widget/v1/?um=constructor%3A04e2289bb03893662710d92abea9a2773afba8eeed0f2203296c9c1ff7fa64be&amp;source=constructor" width="100%" height="400" frameborder="0" ></iframe>
      </div>
  </section>
</template>

<script>
  export default {
    name: 'Contacts',
  }   
  
</script>

<style scoped lang="scss">

@mixin pre-tablet {
     @media (max-width: 975px) { @content; }
}
@mixin pre-mobile {
    @media (max-width: 490px) { @content; }
}
.contacts {
    background: url('../assets/background/bgpattern2.png') repeat;
}
h2 {
    padding-top: 30px;
    padding-bottom: 120px;
    text-align: center;
    font-size: 36px;
    font-weight: 500;
}

.map {
    width: 100%;
    height: 400px;
}

[class*="copyrights-pane"] {
  display: none !important;
}

</style>