<script>
import HomePage from './HomeScreen.vue'
import AboutPage from './AboutPage.vue'

  export default {
    components: {
      HomePage, AboutPage
    },
    data() {
      return {
        curr_screen: 'home'
      }
    }
  }
</script>


<template>
  <body>
    <HomePage @change-page="(n) => curr_screen = n" v-if = "curr_screen === 'home'" />
    <AboutPage @change-page="(n) => curr_screen = n" v-if = "curr_screen === 'about'" />
  </body>
</template>


<style lang="css">

@font-face {
  font-family: "Share Tech Mono", monospace;
  font-weight: 400;
  font-style: normal;
  src: url('https://fonts.googleapis.com/css2?family=Share+Tech+Mono&display=swap');
}

@font-face {
    font-family: 'Noto Sans Display';
    font-style: normal;
    font-weight: 400;
    src: url(../assets/fonts/NotoSansDisplay-Regular.ttf);
}

@font-face {
    font-family: 'VCR OSD MONO';
    src: url(../assets/fonts/VCR_OSD_MONO.ttf);
}

body {
  background: #000;
  color: #eee;

  text-shadow: 0.06rem 0 0.06rem #ea36af, -0.125rem 0 0.06rem #75fa69;
  animation-duration: 0.015s;
  animation-name: textflicker;
  animation-iteration-count: infinite;
  animation-direction: alternate;

  overflow: hidden;

  font-family: "Share Tech Mono", monospace;
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