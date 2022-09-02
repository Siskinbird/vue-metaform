
<template>
    <footer class="footer" id="footer">
        <div class="footer__body container">
            <div class="footer__details">
                    <details>
                        <summary>Телефон</summary>
                        <div class="phones__phones">
                            <p><a href="tel:+74955928790">+7 (495) 592-87-90</a></p>
                            <p><a href="tel:+74955928870">+7 (495) 592-88-70</a></p>
                            <p><a href="tel:+79163739500">+7 (916) 373-95-00</a></p>
                            <p>Ольга Александровна</p>
                        </div>
                    </details>
                    <details>
                        <summary>Наша почта</summary>
                        <div class="webaddress__address">
                        <p><a href="#header"><span>meta</span>form.ru</a></p>
                        <p><a href="mailto:info@metaform.ru">info@<span>meta</span>form.ru</a></p>
                        </div>
                    </details>
                    <details>
                        <summary>Часы работы</summary>
                        <div class="worktime__worktime">
                        <p>Пн - Пт с 9:00 до 17:00</p>
                        <p>Сб - Вс Выходной</p>
                    </div>
                </details>
                <details>
                    <summary>Адрес склада</summary>
                    <address><p><a href="https://goo.gl/maps/tHi1mJHEQse4KCNJ9">
                        Московская обл., г. Химки, микрорайон Сходня, ул. Октябрьская, д.38.</a></p></address>
                </details>
                </div>
            <div class="footer__row">
                <div class="footer__row-phone">
                    <div class="phones__title">
                        <img src="../assets/footericon/phone1.svg" alt="Позвоните нам" class="ico">Телефоны:
                    </div>
                    <div class="phones__line"></div>
                    <div class="phones__phones">
                        <p><a href="tel:+74955928790">+7 (495) 592-87-90</a></p>
                        <p><a href="tel:+74955928870">+7 (495) 592-88-70</a></p>
                        <p><a href="tel:+79163739500">+7 (916) 373-95-00</a></p>
                        <p>Ольга Александровна</p>
                    </div>
                </div>
                <div class="footer__row-worktime">
                    <div class="worktime__title">
                        <img src="../assets/footericon/clock.svg" class="ico" alt="Часы работы"> Часы работы:</div>
                    <div class="worktime__line"></div>
                    <div class="worktime__worktime">
                        <p>Пн - Пт с 9:00 до 17:00</p>
                        <p>Сб - Вс Выходной</p>
                    </div>
                </div>
                <div class="footer__row-web">
                    <div class="webaddress__title">
                        <img src="../assets/footericon/global-network.svg" class="ico" alt="Адрес в интернете"></div>
                    <div class="webaddress__line"></div>
                    <div class="webaddress__address">
                        <p><a href="#header"><span>meta</span>form.ru</a></p>
                        <p><a href="mailto:info@metaform.ru">info@<span>meta</span>form.ru</a></p>
                    </div>
                </div>
            </div>
            <div class="footer__column">
                <div class="barand__image">
                   <a href="#header">
                    <img src="../assets/logo/metaform_full.svg" alt="Производство изделий из проволоки"></a>
                </div>
                
                <div class="brand__copyright"> <img class="ico" src="../assets/footericon/copyright.svg" alt="Все права защищены">2022 Производство изделий из проволоки</div>
            </div>
        </div>
    </footer>
</template>

<script>
    export default {
      name: 'Footer'     
    }
</script>

<style scoped lang="scss">
@mixin tablet-portrait {
  @media (max-width: 600px) { @content; }
}
    .footer {
        max-width: 100%;
        background: url('../assets/background/bgpattern1.png') repeat;
        height: auto;
        padding-top: 40px;
        padding-bottom: 40px;
        color: #ffff;
        font-weight: 400;
            span {
            color: #6CA09F;
            }
    }

    .footer__details {
        display: none;
        @include tablet-portrait {
            display: flex;
            flex-direction: column;
            justify-content: center;
            padding-bottom: 20px;
        }
    }
    .footer__row {
        display: flex;
        justify-content: space-between;
        font-size: 14px;
        font-weight: 500;
        margin-bottom: 20px;
        a {
            color: #ffff;
            text-decoration: none;
            transition: all ease-in-out .4s;
            &:hover {
                color: #00afea;
            }
        }
        img {
            width: 20px;
            height: 20px;
        }
         @include tablet-portrait {
            display: none;
        }
    }
/*     .footer__column {

    } */
    .brand__copyright {
        position: relative;
        width: 53%;
        left: 40px;
        top: -10px;
        display: flex;
        color: #C4c4c4;
        font-size: 11px;
        align-items: center;
        gap: 10px;
        img {
            width: 15px;
            height: 15px;
        }

    }
    .footer__row-phone, .footer__row-worktime, .footer__row-web {
        display: flex;
        gap: 10px; 
    }
    .phones__title, .worktime__title, .webaddress__title {
        display: flex;
        justify-content: flex-start;
        gap: 10px;
    }
    .phones__line {
        border-left: 2px solid #fff;
    }
    .worktime__line, .webaddress__line {
        border-left: 2px solid #fff;
        height: 42%;
    }
    .phones__phones {
        display: flex;
        flex-direction: column;
        gap: 5px;
    }
    details {
        a {
            color: #ffff;
            text-decoration: none;
            transition: all ease-in-out .4s;
            &:hover {
                color: #00afea;
            }
        }
    }

</style>