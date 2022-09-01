<template>
    <section class="contacts">
        <h2>Адрес склада</h2>
        <div id="map" class="map">

        </div>
        <!-- <iframe src="https://yandex.ru/map-widget/v1/?um=constructor%3A04e2289bb03893662710d92abea9a2773afba8eeed0f2203296c9c1ff7fa64be&amp;source=constructor" width="100%" height="350" frameborder="0"></iframe> -->
    </section>
</template>

<script>
    import ymaps from 'ymaps'
    ymaps
    .load('https://api-maps.yandex.ru/2.1/?apikey=60a0e8f7-1d82-44f3-a924-a237ef334c8b&lang=ru_RU')
  .then(maps => {
    const map = new maps.Map('map', {
      center: [55.95180739495034,37.2822959067459],
      zoom: 14
    });
        map.controls.remove('geolocationControl'); // удаляем геолокацию
        map.controls.remove('searchControl'); // удаляем поиск
        map.controls.remove('trafficControl'); // удаляем контроль трафика
        map.controls.remove('typeSelector'); // удаляем тип
        map.controls.remove('fullscreenControl'); // удаляем кнопку перехода в полноэкранный режим
        map.controls.remove('zoomControl'); // удаляем контрол зуммирования
        map.controls.remove('rulerControl'); // удаляем контрол правил
        map.behaviors.disable(['scrollZoom']); // отключаем скролл карты (опционально)
    })
  .catch(error => console.log('Failed to load Yandex Maps', error));


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
    height: 300px;
}

[class*="copyrights-pane"] {
  display: none !important;
}


</style>