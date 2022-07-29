<template>
    <section class="services">
        <div class="services__body">
            <section class="wow slideInLeft" data-wow-duration="2s" data-wow-delay="5s">
            <h2 class="services__body-title animate__animated animate__fadeInLeft">Производство, изготовление и прочие услуги</h2></section>            
        </div>
    </section>
</template>
<!-- <script type="javascript" src="../wow.min.js"></script> -->
<script>
    export default {
      name: 'Services',
      data() {
        return {
            show: false,
            scrollPosition: null
            };
        },
//        created() {
//            window.addEventListener('scroll', this.checkScroll);
//            this.checkScroll();
//        },
//      methods: {
//
//        checkScroll() {
//            this.scrollPosition = window.scrollY;
//                if(this.scrollY >= 500) {
//                    this.show = true;
//                    return;
//                }
//            this.show = false;
//            return;
//        }
//    }
};

</script>


<style scoped lang="scss">

    .services {
        color: #6b6b6b;
    }

    h2 {
        text-align: center;
        font-size: 42px;
        font-weight: 500;
        padding: 5px;
        margin: 60px;
        margin-top: 400px;
        transition: ease-in .9s;
    }
    /* .services__body-title {
        
    } */

/*     .title-enter-active, .title-leave-active {
        //transition: all .9s;
        //transform: translateX(-100%);
        opacity: 0;
    }

    .title-enter, .title-leave-to {
        //transform: translateX(-200%);
        opacity: 1;
    } */

</style>

<!-- Animation -->
<!--  *-enter --> <!-- *-leave -->
<!-- *-enter-active --> <!-- *-leave-active -->
<!-- *-enter-to --> <!-- *-leave-to -->