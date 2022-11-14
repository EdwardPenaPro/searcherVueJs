<template>

<div>
    <div class="masterStyle">
<h1>Search teamates</h1>
<input type="text" v-model="input">

<div class="estilo">
    <ul>
    <li v-for="(name,index) in filteredNames" v-bind:key="index">
        
        {{name}}
        
    </li>
</ul>
</div>


</div>
</div>
</template>

<script>
export default {
name: "userName",
data() {
    
    return {
        names:['Parth','Eduard','Frank','Edger','Max','Chencho','Demian','Alexis','Citalali','Luz','Juan'],
        
        input:""
    }
},
computed:{
    filteredNames(){
        return this.input !== '' ? this.names.filter(name=>name.toLowerCase().includes(this.input.toLowerCase())):''
    }
}
}
</script>

<style scoped>

.masterStyle{
    
    align-content: center;
    border-radius: 10%;
    box-shadow: 10px 5px 5px black;
}
h1{
  font-weight: bold;
  font-size: 30;
  border-radius: 10%;
}
input{
  border: 10%;
  border-width: 1px;
 
}
.estilo{
    
    flex-wrap: wrap;
    width: 400px;
    border-radius: 10%;
    background-color: #eee;
    border-color: black;

}
ul{
    background-color: #eee;
    margin: 1px;
    border-radius: 10%;
    
}
li{
    padding: auto;
    font-weight: bold;
    text-shadow: 1px 1px 2px black;
}
    
</style>

