<template>
    <div class="intro">
        <div class="video">
         <video autoplay muted loop class="video__media">
            <source src="../assets/video/1.mp4" type="video/mp4">
         </video>
        </div>
        <div class="intro__content">
            <div class="intro__block">
                <h1 class="intro__title">МЕТАФОРМ: Дочь,  хочешь заебаться? а заебешься!!!</h1>
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
    top: 0;
    left: 0;
    display: flex;
    flex-direction: column;
    justify-content: center;

    z-index: 3;
    width: 100%;
    height: 100%;
    
}
.intro__block {
    max-width: 1140px;
    margin: 0 auto;
    padding: 0 20px;
}
.intro__title {
    text-align: left;
    font-weight: 600;
    font-size: 45px;
    color: #fff;
    @media(max-width: 600px) {
        font-size: 24px;
    }
    @media(max-width: 410px) {
        padding-top: 40px;
        font-size: 18px;
    }
}
</style>
