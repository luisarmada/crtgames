<script>
    export default {
       
    }
</script>

<template>
    <div id="wrapper">
      <h1 id="myname">Luis Armada</h1>
      <h2 id="subtitle">student & programmer</h2>
      <a @click="$emit('changePage', 'about')" > [ about me ]</a><br>
      <a @click="$emit('changePage', 'portfolio')" > [ my portfolio ]</a><br>
      <a @click="$emit('changePage', 'contacts')"> [ links and contact ] </a> <br>
      <br>
      <a @click="$emit('changePage', 'webgames')"> [ load game ]</a> <br>
    </div>
</template>

<style scoped lang="css">

  #wrapper {
    left: 20%;
    right: 20%;
    position: absolute;
    top: 30%;
    height: 100vh;
    text-align: center;
    font-family: "Share Tech Mono", monospace;
  }

  #myname {
    font-size: 3.9vw;
    letter-spacing: -0.0125em;
    font-weight: 800;
    white-space: nowrap;
    text-align: center;
  }

  #subtitle {
    font-size: 1vw;
    text-align: center;
    margin-top: -1vw;
    margin-bottom: 10px;
    color: #fff;
  }

  a::selection,
  #myname::selection,
  #subtitle::selection{
    color:#000;
    background-color: #eee;
  }

  a {
    cursor: pointer;
    font-size: 1vw;
  }

@media only screen and (max-width: 178vh ) {
  /* change screen space scale when width is not scaling*/
  /* mutliply vw stuff by 1.8. something abt 1920/1080 */
  #myname{
    font-size: 7vh;
  }
  #subtitle{
    font-size: 1.8vh;
  }
  a{
    font-size: 1.8vh;
  }
}
</style>