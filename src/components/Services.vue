<template>
    <section class="services">
        <div class="services__body container">
            <h2 class="services__body-title" data-aos="zoom-in" data-aos-duration="1000">Производство, изготовление и прочие услуги</h2>
            <div class="services__body-items
            container">
                <div class="services-item" data-aos="zoom-in" data-aos-duration="1000">
                    <div class="description">Изготовление комплектующих для других производителей</div>
                </div>
                <div class="services-item" data-aos="zoom-in" data-aos-duration="1000">
                    <div class="description">Выпуск продукции под торговой маркой заказчика</div>
                </div>
                <div class="services-item" data-aos="zoom-in" data-aos-duration="1000">
                    <div class="description">Покраска в любой цвет по цветовой палитре RAL</div>
                </div>
                <div class="services-item" data-aos="zoom-in" data-aos-duration="1000">
                    <div class="description">Изготовление изделий методом штамповки</div>
                </div>
                <div class="services-item" data-aos="zoom-in" data-aos-duration="1000">
                    <div class="description">Рубка листового металла</div>
                </div>
                <div class="services-item" data-aos="zoom-in" data-aos-duration="1000">
                    <div class="description">Гибка круглой и профильной трубы</div>
                </div>
                <div class="services-item" data-aos="zoom-in" data-aos-duration="1000">
                    <div class="description">Производство новых изделий по образцам или эскизам заказчика</div>
                </div>
                <div class="services-item" data-aos="zoom-in" data-aos-duration="1000">
                    <div class="description">Порошковая покраска изделий</div>
                </div>
            </div>          
        </div>
    </section>
</template>
<script>
    export default {
      name: 'Services',
      data() {
        return {
            show: false,
            scrollPosition: null
        };
    }
};

</script>


<style scoped lang="scss">
@mixin tablet-portrait {
  @media (max-width: 543px) { @content; }
}
@mixin tablet-small {
  @media (max-width: 465px) { @content; }
}
    .services {
        color: #6b6b6b;
    }

    h2 {
        text-align: center;
        text-transform: uppercase;
        font-size: 38px;
        font-weight: 500;
        padding: 5px;
        margin: 60px auto;
        transition: ease-in .9s;
        @include tablet-portrait {
            font-size: 28px;
        }
        @include tablet-small {
            font-size: 16px;
            margin: 40px auto;
        }
    }
    .services__body-items {
        display: flex;
        justify-content: space-around;
        flex-direction: row;
        flex-wrap: wrap;

    }
    .description {
        width: 340px;
        height: 102px;
        padding: 10px;
        display: flex;
        justify-content: center;
        font-size: 16px;
        font-weight: 600;
        text-align: center;
        text-transform: uppercase;
        margin: 12px 0 auto auto;
        align-items: center;
        @include tablet-portrait {
            width: 290px;
            font-size: 14px;
            padding: 15px;
            /* display: flex; */
        }
        @include tablet-small {
            font-size: 10px;
            padding: 15px 0 15px 82px;
            margin: 0;
        }
    }

    .services-item {
        cursor: pointer;
        border-radius: 13px;
        width: 471px;
        height: 125px;
        background: url("../assets/services/Group1.svg") 0 0/100% 100% no-repeat;
        //max-width: 100%; 
        margin-top: 20px;
        box-shadow: 8px 8px 10px 0px rgba(34, 60, 80, 0.2);
        transition: all .3s;
        &:hover {
            transform: scale(110%);
        }
        @include tablet-small {
            width: 300px;
            box-shadow: none;
            height: auto;
            margin-top: 0;
        }
    }

    .services-item:nth-child(2n) {
        background: url("../assets/services/group2.svg") 0 0/100% 100% no-repeat;
        .description {
           margin: 8px !important;
           @include tablet-small {
             padding: 15px 77px 15px 0;
        }
        }
        
    }
    
</style>
