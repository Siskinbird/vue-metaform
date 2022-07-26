<template>
    <div class="intro">
        <div class="video">
         <video autoplay muted loop class="video__media">
            <source src="../assets/video/1.mp4" type="video/mp4">
         </video>
        </div>
        <div class="intro__content">
            <div class="intro__block container">
                <h1 class="intro__title">Компания ООО "МЕТАФОРМ"</h1>
                <br><p class="intro__subtitle" >Отечественный производитель сетчатых изделий из проволоки</p>
                <p class="intro__subtitle-description">Применяем современное профессиональное оборудование разных стран (России, Италии и Германии), а также эффективно внедряем передовые технологии в производстве и бизнесе, что позволяет нам быть лидером в выпуске проволочных изделий и изготавливать качественный товар.</p>
            </div>
        </div>
    </div>
</template>

<script>
    export default {
      name: 'VideoBack'     
    }
</script>

<style scoped lang="scss">

.video {
    position: relative;
    padding-bottom: 56%;
    z-index: 1;
    }
.video__media {
    position: absolute;
    top: 0;
    left: 0;
    width:100%;
    height: auto; 
}
.intro {
    position: relative;
    max-height: 50vh;
    overflow: hidden;
    background: url('../assets/video/poster.png') center no-repeat;
    background-size: cover;
}
.intro:after {
    content: '';
    display: block;
    background-color: rgba(0,0,0,.5);
    position: absolute;
    top: 0;
    left: 0;
    z-index: 2;
    width:100%;
    height: 100%;
}
.intro__content {
    position: absolute;
    top: 45%;
    left: 0;
    z-index: 3;
    width: 100%;
    height: auto;
    color: #fff;
    @media(max-width: 1130px) {
        top: 38%;
    }


    @media(max-width: 590px) {
        top: 50%;
    }
    @media(max-width: 340px) {
        top: 60%;
    }
}

.intro__block {
    display: flex;
    justify-content: center;
    flex-direction: column;
    align-items: center;
}

.intro__title {
    text-align: center;
    font-weight: 600;
    font-size: 45px;
    width: 100%;
    @media(max-width: 750px) {
        font-size: 24px;
    }
    @media(max-width: 418px) {
        font-size: 16px;
    }
}

.intro__subtitle {
    padding: 5px;
    margin: 8px auto;
    @media(max-width: 640px) {
        margin: 0 10px;
    }
}
.intro__subtitle-description{
    @media(max-width: 590px) {
        display: none;
    }
}

p {
    text-align: center;
    padding: 5px;
    margin: 5px 8px;
    @media(max-width: 340px) {
        font-size: 10px;
    }
}

</style>
        