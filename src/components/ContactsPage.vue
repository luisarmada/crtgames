<script>

</script>

<template>
    <p id="myemail"> contact: luisarmada44@gmail.com </p>
    <div id="contacts_type_select">
        
        <div class="socialsection_select">
            <img src="./icons/github_icon3.png" class="invertcol"></img>
            
            <span>
                <h2>GitHub</h2>
                <p> Publicly accessible repositories of my past projects. </p>
            </span>
            
        </div>
        <div class="socialsection_select_b">
            
            
            <span>
                <h2>YouTube</h2>
                <p> Development logs and tutorials. </p>
            </span>
            <img src="./icons/github_icon3.png"></img>
        </div>
        <div class="socialsection_select">
            <img src="./icons/github_icon3.png" class="invertcol"></img>
            
            <span>
                <h2>Itch.io</h2>
                <p> Various game projects uploaded on here, from game jams to collaborations. </p>
            </span>
            
        </div>
        <div class="socialsection_select_b">
            
            
            <span>
                <h2>LinkedIn</h2>
                <p> Connect with me and see my past experiences. </p>
            </span>
            <img src="./icons/github_icon3.png"></img>
        </div>
        
    </div>
    
    <div id="backbutton">
      <a @click="$emit('changePage', 'home')">[ back ]</a>
    </div>
</template>

<style scoped>
#myemail{
    position: absolute;
    top: 15px;
    left: 0;
    width: 100%;
    text-align: center;
    color: #00FF00;
}

.invertcol {
    -webkit-filter: invert(100%); /* Safari/Chrome */
    filter: invert(100%);
    object-fit: contain;
    
}

#contacts_type_select{
    position:absolute;
    top: 10%;
    left: 8%;
    right: 8%;
    bottom: 15%;
    display: flex;
    flex-direction: column;
}

#contacts_type_select h2{
    text-decoration: underline;
}

.socialsection_select {
    flex: 1;
    display: flex;
    text-align: center;
    cursor: pointer;
    max-height: 25%;
    padding-bottom: 10px;
    gap: 10px;
}

.socialsection_select:hover {
    border: 2px solid white;
}

.socialsection_select_b {
    flex: 1;
    display: flex;
    text-align: center;
    cursor: pointer;
    max-height: 25%;
    padding-bottom: 10px;
    gap: 10px;
    background-color: #ddd;
    color: #111;
}

.socialsection_select_b:hover{
    border: 2px solid black;
}

#games_select:hover{
    background-color: #ddd;
    color: #111;
}

.socialsection_select_b span,
.socialsection_select span{
    flex: 1;
}

#backbutton {
    position: absolute;
    width: 100%;
    text-align: center;
    left: 0;
    bottom: 7%;
    cursor: pointer;
}

</style>