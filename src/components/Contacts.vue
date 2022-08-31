<template>
    <div class="contacts">
        <div class="contacts__body container"><h2>Контакты</h2>
            <div class="address__item">
                <div class="moscow address">
                    <div class="moscow__title"><h3>Головной офис и основной склад</h3></div>
                    <div class="moscow__subtitle"><address><p>Московская обл., г. Химки, микрорайон Сходня, ул. Октябрьская, д.38. </p></address></div>
                </div>
                <div class="moscow map">
                    <iframe src="https://www.google.com/maps/embed?pb=!1m14!1m8!1m3!1d1116.9213628311957!2d37.28172089597332!3d55.95209778565299!3m2!1i1024!2i768!4f13.1!3m3!1m2!1s0x46b53fc7dba4f6a9%3A0x992f37f7bdfeaffe!2z0YPQuy4g0J7QutGC0Y_QsdGA0YzRgdC60LDRjyAo0KHRhdC-0LTQvdGPKSwgMzTQkCwg0KXQuNC80LrQuCwg0JzQvtGB0LrQvtCy0YHQutCw0Y8g0L7QsdC7LiwgMTQxNDIw!5e0!3m2!1sru!2sru!4v1638115386457!5m2!1sru!2sru" width="469" height="225" style="border:0; border-radius: 8px;" allowfullscreen="" loading="lazy">
                    </iframe>
                </div>
            </div> 
            <div class="address__item">
                <div class="orel address">
                    <div class="orel__title"><h3>Собственная производственная база</h3></div>
                    <div class="orel__subtitle"><address><p>г. Орел, ул. Раздольная, д. 105.</p></address></div>
                </div>
                <div class="orel map">
                    <iframe src="https://www.google.com/maps/embed?pb=!1m14!1m8!1m3!1d2398.6815316960715!2d36.1569128!3d53.0440607!3m2!1i1024!2i768!4f13.1!3m3!1m2!1s0x41321784ff4606e9%3A0x67760f3b5501bd2e!2zedC70LjRhtCwINCg0LDQt9C00L7Qu9GM0L3QsNGPLCAxMDUsINCe0YDRkdC7LCDQntGA0LvQvtCy0YHQutCw0Y8g0L7QsdC7LiwgMzAyMDM4!5e0!3m2!1sru!2sru!4v1638171046755!5m2!1sru!2sru" width="469" height="225" style="border:0; border-radius: 8px;" allowfullscreen="" loading="lazy"></iframe>
                </div>
            </div>              
            </div>
    </div>
</template>

<script>
    export default {
      name: 'Contacts'     
    }
</script>

<style scoped lang="scss">

@mixin pre-tablet {
  @media (max-width: 975px) { @content; }
}
@mixin pre-mobile {
  @media (max-width: 490px) { @content; }
}
.contacts__body {
    display: flex;
    align-items: center;
    justify-content: center;
    flex-direction: column;
    padding: 60px 0;
    margin: 0 auto;
    h2 {
        font-size: 42px;
        text-align: center;
        padding-bottom: 25px;
        margin: 60px auto;
    }
}
.address__item {
    display: flex;
    align-items: center;
    justify-content: space-between;
    text-transform: uppercase;
    h3 {
    font-size: 16px;
    font-weight: 800;
    color: #6B6B6B;
    line-height: 118%;
    }
    @include pre-tablet {
        flex-wrap: wrap;
        justify-content: center;
    }
    @include pre-mobile {
        width: 90%;
    }
}

.address {
    width: 470px;
    height: 225px;
    border: 1px splid #6B6B6B;
    padding: 24px 74px 76px 28px;
    max-width: 100%;
    border-radius: 8px;
    background-color: #F1F1F1;
    margin: 10px;
    text-align: left;
    transition: .5s;
    &:hover {
        box-shadow: 0 0 10px #6B6B6B;
    }
}

iframe {
    width: 100%;
    transition: .5s;
    &:hover {
        box-shadow: 0 0 10px #6B6B6B;
        border-radius: 8px;
    }
}

</style>