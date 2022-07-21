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
    position: fixed;
    right: 0;
    bottom: 0;
    min-width: 100%;
    height: auto;
}
</style>