<template>
  <div id="masterContainer">
    
   

    
    <div class="masterContainer">
        <div class="rectangle">
            
    <div class="character" v-for="character in characters.results" :key="character.id">
         <div class="characterName">
            <img class="characterImg" :src="character.image" alt="character.name">
            <div class="data">
                
                
                <h2 ref="#" >{{character.name}}</h2> 
                <h3 ref="#">{{character.species}}</h3>
                <h4 ref="#">{{character.gender}}</h4>
                <h5 ref="#">{{character.location.name}}</h5>
                <div class="row">
                    <span id="status" class="green" v-if="character.status=='Alive'"></span>
                    <span id="status" class="red" v-else-if="character.status=='Dead'"></span>
                <h6 ref="#">{{character.status}}</h6> 
                </div>
            </div>
            
            
            </div>
    
        </div>

<!-- {{ character.name }} -->
    </div>
    
    </div>
  </div>
</template>
<script>
export default {
   name:"rickAndMorty",
   data(){
       return{ characters: []}
},
methods: {
   callingAPI(){
       fetch("https://rickandmortyapi.com/api/character").then(res => res.json().then((data)=>{
           this.characters = data
       }))
   }


},
mounted() {
   this.callingAPI()
}

}
</script>

<style scoped>
h1{
    font-weight: bold;
    color: #eee;
    font-size: 24px;

}
#masterContainer{
    display: flex;
    justify-content: center;
    align-content: center;
    background-color: rgb(0, 0, 0);
    text-align: center;


}
.masterContainer{
    display: flex;
    flex-wrap: wrap;
    align-content: center;
}

.rectangle{
    display: flex;
    border-radius: 30%;
    background-color: greenyellow;
    
    align-content: center;
    justify-content: center;
    flex-wrap: wrap;
    flex-direction: inherit;
    
}

.character{
        width: 500px;
        border-radius: 5%;
         display: flex;
         flex-direction: row;
         padding: 1%;

}
.character:hover {
box-shadow: 0px 3px 14px 0px rgba(44, 198, 36, 0.75);
-webkit-box-shadow: 0px 3px 14px 0px rgba(61, 210, 27, 0.75);
-moz-box-shadow: 0px 3px 14px 0px rgba(85, 255, 0, 0.819);
}

.data{
    padding-left: 10px;
}
.characterImg{
    border-radius: 5%;
    
}
.characterName{
    display: flex;
    text-align: center;
    color: aliceblue;
    text-shadow: 2px 2px 5px rgb(13, 225, 87);
}
h2:hover{
color: green;
}

#status{
    display: inline-flex;
    height: 10px;
    width: 10px;
    border-radius: 50%;
}
.green{
    background-color:green ;
}
.red{
    background-color: red;
}
.row{
    display: inline-flex;   

}
</style>