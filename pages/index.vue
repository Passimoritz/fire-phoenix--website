<template>
  <div class="main">
    <img class="image" src="../assets/images/phoenix.png">
    <video class="video" src="../assets/videos/main.mp4" autoplay loop muted />
  </div>
</template>

<script>

</script>

<style lang="scss">
body {
  overflow: hidden;
}
.main {
  text-align: center;
}

.video {
  position: absolute;
  top: 0;
  left: 0;
  opacity: 0;
  transition: 3.4s;
}

.image {
  z-index: 1;
  position: absolute;
  left: 0;
  right: 0;
  margin: 0 auto;
  margin-top: 40px;
  width: 40%;
  transition: 1.4s;

  &:hover {
    opacity: 0;

    &+ .video {
      opacity: 1;
    }
  }
}

</style>
