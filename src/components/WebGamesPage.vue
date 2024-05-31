<script>
    export default {
      data() {
        return {
          isHover: 0,
          items: [
          {title: "HOME", type: "(DIR)"},
            {title: "Pong.exe", type: "(LOAD)"},
            {title: "FalloutTerminal.exe", type: "(LOAD)"},
            {title: "Snake.exe", type: "(LOAD)"},
          ]
        }
      },
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
      <!--<iframe frameborder="0" src="https://itch.io/embed-upload/10512734?color=0f0f0f" allowfullscreen="" width="100%" height="100%"><a href="https://luisarmada.itch.io/the-right-of-revenge">Play The Right of Revenge on itch.io</a></iframe>-->
      <h2 id="urlsubtitle">Parent directory</h2>

      <div v-for="(item, index) in items" @mouseover="isHover = index" class="gameoption" :class="{'selectedgameoption' : isHover === index}"> <h2 class="gameurlselector">>&nbsp;</h2> 
        <h2 class="gametitle">{{ item.title }}</h2> <h2 class="gamefiletype">{{ item.type }}</h2>
      </div>
      
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
        cursor: pointer;
    }
    .gameoption h2{
        font-size: 1.2vw;
    }

    .selectedgameoption {
        color: #00FF00;
    }

    .selectedgameoption .gameurlselector{
      opacity: 1;
    }

    .gametitle{
        text-align: left;
    }

    .gamefiletype{
        text-align: right;
        flex: 1;
    }

    .gameurlselector {
      opacity: 0;
    }

  #wrappergame {
    position: absolute;
    top: 25px;
    left: 10%;
    height: 100%;
    right: 10%;
    margin-left: -1.4vw;
  }

  #gameurl {
    font-size: 1.5vw;
    white-space: nowrap;
    text-align: center;
    color: #00FF00;
    margin-left: 1.4vw;
  }

  #urlsubtitle{
    text-align: left;
    font-size: 1.2vw;
    margin-left: 1.4vw;
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
    margin-left: 1.4vw;
  }

@media only screen and (max-width: 178vh ) {
  /* change screen space scale when width is not scaling*/
  /* mutliply vw stuff by 1.8. something abt 1920/1080 */
  
}
</style>