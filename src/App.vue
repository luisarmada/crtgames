<script>
import CRTOverlay from './components/CRTOverlay.vue'

export default{
  components: {
    CRTOverlay
  }
}
</script>

<template>
  <body>
    <div id="bgblock"></div>
    <div id="monitor">
      <div id="screenspace">
        <CRTOverlay />
      </div>
      <img src="./assets/c1902bedroom_glare.png" />
    </div>
  </body>
</template>

<style scoped>
#bgblock {
  position: absolute;
  left: 0;
  top: 0;
  width: 100vw;
  height: 100vh;
  background: #111;
}

body {
  overflow: hidden;
  background: #003321;
}

#monitor{
  position: absolute;
  left: 0;
  top: 0;
  width: 100vw;
  height: 100vh;
  display: grid;
}

#monitor img {
  width: 100%;
  height: 100%;
  object-fit: cover;
  pointer-events: none;
  user-select: none;
  object-position: bottom;
  z-index: 11;
}

#screenspace {
  position: absolute;
  width: 50vw;
  height: 37vw;
  bottom: 9.5vw;
  left: 50%;
  transform:translate(-50%, 0);
  z-index: 10;
}

@media only screen and (max-width: 178vh ) {
  /* change screen space scale when width is not scaling*/
  #screenspace{
    bottom: calc(100%  - 83%);
    width: 90vh;
    /*right: 0;*/
    height: 66vh;
  }
}

</style>
