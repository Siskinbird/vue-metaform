<template>
  <section class="contacts">
      <h2>Адрес склада</h2>
      <div class="address__body container">
        <a href="https://yandex.ru/maps/-/CCUVY-AioC" data-aos="zoom-in" data-aos-duration="1000"><div class="address__body-item">
          <h3>Головной офис и основной склад</h3>
          <address> Московская обл., г. Химки, микрорайон Сходня, ул. Октябрьская, д.38.</address>
        </div></a>
        <a href="https://yandex.ru/maps/-/CCUVY-u-pB" data-aos="zoom-in" data-aos-duration="1000"><div class="address__body-item">
          <h3>Собственная производственная база</h3>
          <address>г. Орел, ул. Раздольная, д. 105.</address>
        </div></a>
      </div>
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
@mixin mobile {
    @media (max-width: 590px) { @content; }
}
@mixin mobile-s {
    @media (max-width: 400px) { @content; }
}
.contacts {
    background: url('../assets/background/bgpattern2.png') repeat;
}
h2 {
    padding-top: 30px;
    padding-bottom: 60px;
    text-align: center;
    font-size: 36px;
    font-weight: 500;
}
h3 {
  font-weight: 500;
  margin-bottom: 10px;
}

.map {
    width: 100%;
    height: 400px;
}

.address__body {
  display: flex;
  align-items: center;
  justify-content:center;
  gap: 50px;
  padding-bottom: 40px;
  @include mobile {
    flex-direction: column;
  }
}
  a {
    color: #6b6b6b;
    text-decoration: none;
    transition: all ease-in-out .4s;
    &:hover {
    color: #00afea;
    }
  }
.address__body-item {
  transition: all ease-in-out .4s;
  cursor: pointer;
  padding: 10px;
  width: 390px;
  border: 2px solid #6ca09f;
  border-radius: 12px;
  background-color: #fff;
  height: 127px;
  &:hover {
    margin-top: -10px;
    box-shadow: 8px 8px 10px 0px rgba(34, 60, 80, 0.2);
  }
  @include mobile-s {
    width: 310px;
    height: 140px;
  }
}
iframe {
  margin-top: 20px;
}

</style>