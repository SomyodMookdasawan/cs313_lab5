<template>
  <div id="app">
    <img alt="bg" src="./assets/bg.jpg">
    <h1>The Infinity War Game</h1>
     <div class="row">
      <button @click="ramdomDamage" class="btn btn-info" >start</button>
      <button @click="ramdomDamage" class="btn btn-info" >Attack</button>
      <button @click="ramdomDamage" class="btn btn-info" >Special Attack</button>
    </div>
  </div>
  
</template>

<script>
export default {
  name: 'App',
  data : function(){
        return{
            classObject: {
                active: true,
                "text-danger": false,
                weight: 20,
            },
            player:[
                {name:'naruto', hp:150, image:''},
                {name:'asta', hp:120, image:''},
                {name:'red demon', hp:100, image:''},
                {name:'tanjiro', hp:110, image:''},
            ],
            monster:[
                {name:'dabi', hp:130, image:''},
                {name:'qoo', hp:110, image:''},
                {name:'spinner', hp:100, image:''},
                {name:'rappa', hp:100, image:''}
            ],
        }
    },
    methods : {
        ramdomDamage: function(min ,max){
            this.ramdomNo = Math.max(Math.floor(Math.ramdom()*max)+1,min)
        },
    },
}
</script>

<style>
#app {
  font-family: Avenir, Helvetica, Arial, sans-serif;
  -webkit-font-smoothing: antialiased;
  -moz-osx-font-smoothing: grayscale;
  text-align: center;
  color: #2c3e50;
  margin-top: 60px;
}
</style>
