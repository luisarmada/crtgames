<script>

</script>

<template>
    <body>
    <div id="wrapper">
      <h1 id="myname">Luis Armada</h1>
      <h2 id="subtitle">student & programmer</h2>
      <a> about_me</a>
      <a> my_projects</a>
      <a> blog</a>
      <a> extra_games</a> <br>
      <a> contact </a>
    </div>
  </body>
</template>

<style>
 @font-face {
    font-family: 'Noto Sans Display';
    font-style: normal;
    font-weight: 400;
    src: url(../assets/NotoSansDisplay-Regular.ttf);
  }
  body {
    font-family: 'Noto Sans Display';
    
    background: #000;
    color: #eee;

    text-shadow: 0.06rem 0 0.06rem #ea36af, -0.125rem 0 0.06rem #75fa69;
    animation-duration: 0.015s;
    animation-name: textflicker;
    animation-iteration-count: infinite;
    animation-direction: alternate;

    overflow: hidden;
  }
  #wrapper {
    width: 23vw;
    left: 50%;
    transform: translate(-50%, 0);
    position: absolute;
    top: 35%;
    height: 100vh;
    text-align: center;
  }

  #myname {
    font-size: 4vw;
    letter-spacing: -0.0125em;
    font-weight: 800;
  }

  #subtitle {
    font-size: 1vw;
    text-align: right;
    margin-top: -20px;
    margin-bottom: 10px;
  }

  a::selection,
  #myname::selection,
  #subtitle::selection{
    color:#000;
    background-color: #eee;
  }

  a {
    cursor: pointer;
  }

  @keyframes textflicker {
    from {
      text-shadow: 1px 0 0 #ea36af, -2px 0 0 #75fa69;
    }
    to {
      text-shadow: 2px 0.5px 2px #ea36af, -1px -0.5px 2px #75fa69;
    }
  }
</style>