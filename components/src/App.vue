<template>
<div>
<ClickCounter/>
<HoverCounter/>
</div>
</template>

<script>
import HoverCounter from './components/HoverCounter.vue'
import ClickCounter from './components/ClickCounter.vue'
export default {
  
  name: 'App',
  data(){
    return{
     name:""
       
    } 
  },
  methods: {
   
  },
  components: {
     
    HoverCounter,
    ClickCounter
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
