<template>
    <div class="video-player">
        <video autoplay muted loop id="myVideo">
            <source src="../assets/video/1.mp4" type="video/mp4">
        </video>
    </div>
</template>

<script>
    export default {
      name: 'VideoBack'     
    }
</script>

<style scoped lang="scss">
    #myVideo {
    position: relative;
    /* filter: opacity(70%); */
    filter: grayscale(70%);
    top:60px;
    right: 0;
    bottom: 0;
    max-width: 100%;
    height: auto;
}
</style>