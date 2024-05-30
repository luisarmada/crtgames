<script>
    export default {
        methods: {
            ChangePage(newpage) {
                this.$emit('about', curr_screen);
                alert('Hello');
            }
        }
    }
</script>

<template>
    <div id="wrappergame">
      <h1 id="gameurl"> C:/USERS/luisarmada/my_games/</h1>
      <h2 id="urlsubtitle">Parent directory</h2>
      <div class="gameoption selectedgameoption"> <h2 class="gameurlselector">>&nbsp;</h2> <h2 class="gametitle">HOME</h2> <h2 class="gamefiletype">(DIR)</h2> </div>
      <div class="gameoption"> <h2 class="gametitle">Pong.exe</h2> <h2 class="gamefiletype">(LOAD)</h2> </div>
      <div class="gameoption"> <h2 class="gametitle">FalloutTerminal.exe</h2> <h2 class="gamefiletype">(LOAD)</h2> </div>
      <div class="gameoption"> <h2 class="gametitle">Snake.exe</h2> <h2 class="gamefiletype">(LOAD)</h2> </div>
      <div class="gameoption"> <h2 class="gametitle">Tetris.exe</h2> <h2 class="gamefiletype">(LOAD)</h2> </div>
      
      <div id="backbutton">
      <a @click="$emit('changePage', 'home')">[ back ]</a>
      </div>
    </div>
</template>

<style scoped>

    .gameoption{
        display: flex;
        align-items: stretch;
        width: 100%;
    }
    .gameoption h2{
        font-size: 1.2vw;
    }

    .selectedgameoption {
        color: #00FF00;
    }

    .gametitle{
        text-align: left;
    }

    .gamefiletype{
        text-align: right;
        flex: 1;
    }

  #wrappergame {
    position: absolute;
    top: 25px;
    left: 10%;
    height: 100%;
    right: 10%;
  }

  #gameurl {
    font-size: 1.5vw;
    white-space: nowrap;
    text-align: center;
    color: #00FF00;
  }

  #urlsubtitle{
    text-align: left;
    font-size: 1.2vw;
  }

  a::selection,
  #myname::selection,
  #subtitle::selection{
    color:#000;
    background-color: #eee;
  }

  #backbutton {
    cursor: pointer;
    font-size: 1vw;
    text-align: center;
  }

@media only screen and (max-width: 178vh ) {
  /* change screen space scale when width is not scaling*/
  /* mutliply vw stuff by 1.8. something abt 1920/1080 */
  
}
</style>