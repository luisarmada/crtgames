<script>
export default {
    
}
</script>

<template>
<body>
  <div id="monitor">
    
    <div id="screenspace">

    </div>
    <img src="../assets/jcpennybedroom_scratched.png" />
  </div>
</body>
</template>

<style lang="css">
body {
  overflow: hidden;
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
  right: 25vw;
  height: 37vw;
  bottom: 9.5vw;
  left: 25vw;
  z-index: 10;
  background-color: green;
}



@media only screen and (max-width: 178vh ) {
  #screenspace{
    background-color: blue;
    bottom: calc(100%  - 83%);
    left: 0;
    right: 0;
    height: 66vh;
  }
}
@media only screen and (max-width: 89vh ) {
  #screenspace{
    background-color: red;
    bottom: calc(100%  - 83%);
    left: 0vw;
    right: 0vw;
    height: 66vh;
  }
}
</style>