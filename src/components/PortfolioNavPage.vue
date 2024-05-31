<script>

</script>

<template>
    <div id="portfolio_type_select">
        <div id="games_select">
            <span>

            </span>
            <h2>games</h2>
        </div>
        <div id="apps_select">
            <span>

            </span>
            <h2>sites & apps</h2>
        </div>
    </div>
    
    <div id="backbutton">
      <a @click="$emit('changePage', 'home')">[ back ]</a>
    </div>
</template>

<style scoped>

#portfolio_type_select{
    position:absolute;
    top: 10%;
    left: 10px;
    right: 10px;
    bottom: 15%;
    display: flex;
}

#games_select {
    flex: 1;
    display: flex;
    flex-direction: column;
    margin-left: 4%;
    margin-right: 2%;
    text-align: center;
    cursor: pointer;
    
}

#games_select:hover{
    background-color: #ddd;
    color: #111;
}

#games_select span{
    background-color: violet;
    border: 2px solid #eee;
    flex: 1;
}

#apps_select {
    flex: 1;
    display: flex;
    margin-right: 4%;
    margin-left: 2%;
    flex-direction: column;
    text-align: center;
    cursor: pointer;
}

#apps_select:hover{
    background-color: #ddd;
    color: #111;
}

#apps_select span{
    background-color: gray;
    flex: 1;
    border: 2px solid #eee;
}

#backbutton {
    position: absolute;
    width: 100%;
    text-align: center;
    left: 0;
    bottom: 9%;
    cursor: pointer;
}

</style>