<template>
<div>
 <childstyles/>
 <NamedList/>
 <h4>App Component</h4>
</div>
 
</template>

<script>
import NamedList from './components/NamedList.vue'
import Childstyles from './components/Childstyles.vue'
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
    NamedList,
    Childstyles
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
