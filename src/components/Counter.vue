<template>
  <div>
      <button @click="ramdomDamage" class="btn btn-info" >{{lable}}</button>
  </div>
  
</template>

<script>
export default {
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
    props: {
        label : String,
    },

    methods : {
        ramdomDamage: function(min ,max){
            this.ramdomNo = Math.max(Math.floor(Math.ramdom()*max)+1,min)
        },
    },

}
</script>

<style>

</style>