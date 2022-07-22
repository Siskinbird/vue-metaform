<template>
    <div class="intro">
        <div class="video-player">
         <video autoplay muted loop id="myVideo">
                <source src="../assets/video/1.mp4" type="video/mp4">
         </video>    
        </div>
    </div>
</template>

<script>
    export default {
      name: 'VideoBack'     
    }
</script>

<style scoped lang="scss">

.video-player {
    position: relative;
    padding-bottom: 56%;
    z-index: 1;
    }
#myVideo {
    position: absolute;
    top: 0;
    left: 0;
    width:100%;
    height: auto; 
}
.intro {
    position: relative;
    max-height: 60vh;
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
</style>
