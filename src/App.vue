<template>
  <div id="app"> 
 <TestMyVue></TestMyVue>
  
  </div>
</template>
<script>

import TestMyVue from "./myapi.vue"

export default {
  name: 'app',
  components: {
    TestMyVue
    
  }
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
