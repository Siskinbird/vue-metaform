<template>
    <section class="services">
        <div  data-aos="fade-right">
            <div class="services__body">
             <h2 class="services__body-title">Производство, изготовление и прочие услуги</h2>           
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

        <!-- created() {
            window.addEventListener('scroll', this.checkScroll);
            this.checkScroll();
        },
      methods: {

        checkScroll() {
            this.scrollPosition = window.scrollY;
                if(this.scrollY >= 500) {
                    this.show = true;
                    return;
                }
            this.show = false;
            return;
        }
    } -->