<script>
    import ScreenContents from './ScreenContents.vue'
    
    export default {
    components: {
        ScreenContents
    }
    }
</script>

<template>
    <input type="checkbox" id="switch" checked>
    <label for="switch" class="switch-label"> </label> 
   

    <div class="container">
    
        <div class="screen">
            <ScreenContents />
        </div>
    <div class="overlay">AV-1</div>
    </div>
</template>

<style scoped lang="css">


body {
  background: #111;
  color: white;
  padding-top: 20px;
  padding-left: 20px;
}

#switch {
  display: none;
}

.switch-label {
  display: inline-block;
  cursor: pointer;
  background: #fff;
  color: #111;
  padding: 10px;
  padding-left: 15px;
  padding-right: 15px;
  border-radius: 5px;
  margin-top: 10px;
  box-shadow: 0 2px #666;
}
.switch-label::after {
  content: "on";
}
.switch-label::before {
  content: " ";
  display: inline-block;
  border-radius: 100%;
  width: 10px;
  height: 10px;
  background: #003321;
  margin-right: 10px;
  border: 1px solid #111;
}
.switch-label:active {
  box-shadow: none;
  transform: translate3d(0, 2px, 0);
}

#switch:checked + .switch-label::before {
  background: #22ff55;
}
#switch:checked + .switch-label::after {
  content: "off";
}

@keyframes flicker {
  0% {
    opacity: 0.56949;
  }
  5% {
    opacity: 0.90146;
  }
  10% {
    opacity: 0.76675;
  }
  15% {
    opacity: 0.02496;
  }
  20% {
    opacity: 0.5217;
  }
  25% {
    opacity: 0.77937;
  }
  30% {
    opacity: 0.68842;
  }
  35% {
    opacity: 0.05909;
  }
  40% {
    opacity: 0.0258;
  }
  45% {
    opacity: 0.26189;
  }
  50% {
    opacity: 0.67488;
  }
  55% {
    opacity: 0.52841;
  }
  60% {
    opacity: 0.65677;
  }
  65% {
    opacity: 0.4096;
  }
  70% {
    opacity: 0.9573;
  }
  75% {
    opacity: 0.83145;
  }
  80% {
    opacity: 0.14949;
  }
  85% {
    opacity: 0.515;
  }
  90% {
    opacity: 0.60339;
  }
  95% {
    opacity: 0.02453;
  }
  100% {
    opacity: 0.62779;
  }
}
.container {
  background: #121010;
  width: 100%;
  height: 100%;
  margin-top: -50px;
  position: relative;
  overflow: hidden;
}
.container::after {
  content: " ";
  display: block;
  position: absolute;
  top: 0;
  left: 0;
  bottom: 0;
  right: 0;
  background: rgba(18, 16, 16, 0.1);
  opacity: 0;
  z-index: 2;
  pointer-events: none;
}
.container::before {
  content: " ";
  display: block;
  position: absolute;
  top: 0;
  left: 0;
  bottom: 0;
  right: 0;
  background: linear-gradient(rgba(18, 16, 16, 0) 50%, rgba(0, 0, 0, 0.25) 50%), linear-gradient(90deg, rgba(255, 0, 0, 0.06), rgba(0, 255, 0, 0.02), rgba(0, 0, 255, 0.06));
  z-index: 2;
  background-size: 100% 2px, 3px 100%;
  pointer-events: none;
}

#switch:checked ~ .container::after {
  animation: flicker 0.15s infinite;
}

@keyframes turn-on {
  0% {
    transform: scale(1, 0.8) translate3d(0, 0, 0);
    -webkit-filter: brightness(30);
    filter: brightness(30);
    opacity: 1;
  }
  3.5% {
    transform: scale(1, 0.8) translate3d(0, 100%, 0);
  }
  3.6% {
    transform: scale(1, 0.8) translate3d(0, -100%, 0);
    opacity: 1;
  }
  9% {
    transform: scale(1.3, 0.6) translate3d(0, 100%, 0);
    -webkit-filter: brightness(30);
    filter: brightness(30);
    opacity: 0;
  }
  11% {
    transform: scale(1, 1) translate3d(0, 0, 0);
    -webkit-filter: contrast(0) brightness(0);
    filter: contrast(0) brightness(0);
    opacity: 0;
  }
  100% {
    transform: scale(1, 1) translate3d(0, 0, 0);
    -webkit-filter: contrast(1) brightness(1.2) saturate(1.3);
    filter: contrast(1) brightness(1.2) saturate(1.3);
    opacity: 1;
  }
}
@keyframes turn-off {
  0% {
    transform: scale(1, 1.3) translate3d(0, 0, 0);
    -webkit-filter: brightness(1);
    filter: brightness(1);
    opacity: 1;
  }
  60% {
    transform: scale(1.3, 0.001) translate3d(0, 0, 0);
    -webkit-filter: brightness(10);
    filter: brightness(10);
  }
  100% {
    animation-timing-function: cubic-bezier(0.755, 0.05, 0.855, 0.06);
    transform: scale(0, 0.0001) translate3d(0, 0, 0);
    -webkit-filter: brightness(50);
    filter: brightness(50);
  }
}
.screen {
  width: 100%;
  height: 100%;
  border: none;
  opacity: 0;
}

#switch ~ .container > .screen {
  animation: turn-off 0.55s cubic-bezier(0.23, 1, 0.32, 1);
  animation-fill-mode: forwards;
}

#switch:checked ~ .container > .screen {
  animation: turn-on 4s linear;
  animation-fill-mode: forwards;
  animation-delay: 1s;
}

@keyframes overlay-anim {
  0% {
    visibility: hidden;
  }
  20% {
    visibility: hidden;
  }
  21% {
    visibility: visible;
  }
  100% {
    visibility: hidden;
  }
}
.overlay {
  color: #00FF00;
  position: absolute;
  top: 20px;
  left: 40px;
  font-size: 60px;
  visibility: hidden;
  pointer-events: none;
}

#switch:checked ~ .container .overlay {
  animation: overlay-anim 5s linear;
  animation-fill-mode: forwards;
  
}

</style>