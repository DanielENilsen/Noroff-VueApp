    
<template>
   <div class="[ row ]">    
       <div v-for="res in recipe" class="[ col-sm-12 ]"> 
            <TestMyVue  
                v-bind:title="res.title"
                v-bind:href="res.href"
                v-bind:ingredients="res.ingredients"
                v-bind:thumbnail="res.thumbnail"                                                    
            ></TestMyVue>      
                      
        </div>  
    </div>       
</template>

<script>
import TestMyVue from "./components/testmy.vue";


export default {
        
    name: "myresipy",
        components:{
            TestMyVue
        },
        data() {
            return {
                recipe:[]
            }
        },
        beforeMount: function () {
            const myApp = this;
           
            const corsURL = 'https://cors-anywhere.herokuapp.com/';
            const link = "http://www.recipepuppy.com/api/"
            
                fetch(corsURL  + link ).then(function(reponsive) { 
                    return reponsive.json()
                }).then(function(result) { 
                    myApp.recipe = result;
                })
        }
}




</script>


