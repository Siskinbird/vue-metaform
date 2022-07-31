<template>
    <section class="services">
        <div class="services__body">
            <h2 class="services__body-title" data-aos="fade-right" data-aos-duration="1000">Производство, изготовление и прочие услуги</h2>
            <div class="services__body-items
            container">
                <div class="services-item" data-aos="fade-right" data-aos-duration="1000">
                    <div class="description">Изготовление комплектующих для других производителей</div>
                </div>
                <div class="services-item" data-aos="fade-left" data-aos-duration="1000">
                    <div class="description">Выпуск продукции под торговой маркой заказчика</div>
                </div>
                <div class="services-item" data-aos="fade-right" data-aos-duration="1000">
                    <div class="description">Покраска в любой цвет по цветовой палитре RAL</div>
                </div>
                <div class="services-item" data-aos="fade-left" data-aos-duration="1000">
                    <div class="description">Изготовление изделий методом штамповки</div>
                </div>
                <div class="services-item" data-aos="fade-right" data-aos-duration="1000">
                    <div class="description">Рубка листового металла</div>
                </div>
                <div class="services-item" data-aos="fade-left" data-aos-duration="1000">
                    <div class="description">Гибка круглой и профильной трубы</div>
                </div>
                <div class="services-item" data-aos="fade-right" data-aos-duration="1000">
                    <div class="description">Производство новых изделий по образцам или эскизам заказчика</div>
                </div>
                <div class="services-item" data-aos="fade-left" data-aos-duration="1000">
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

        @media(max-width: 620px) {
            font-size: 34px;
            margin: 30px auto;
        }
        @media(max-width: 450px) {
            font-size: 28px;
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
        @media(max-width: 446px) {
            font-size: 12px;
                       
        }
        @media(max-width: 440px) {
            width: 236px; 
            font-size: 10px;        
        }
    }
    /* .description:nth-child(2n) {
        align-items: flex-start;
    } */
    .services-item {
        cursor: pointer;
        width: 471px;
        height: 125px;
        background: url("../assets/services/Group1.svg") 0 0/100% 100% no-repeat;
        max-width: 100%; 
        margin-top: 20px;
    }
    .services-item:nth-child(2n) {
        background: url("../assets/services/group2.svg") 0 0/100% 100% no-repeat;
        .description {
           margin: 8px !important;
        }
    }
    
</style>
