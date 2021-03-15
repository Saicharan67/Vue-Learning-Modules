<template>
<div>
 <p>Hello {{name}}</p>
 <p v-text="college"> </p> <!--v-bind-->
 <p v-html="htmlbinding"></p><!--v-text-->
 <h2 v-bind:id="headingID">Heading</h2>
 <h2 v-bind:class="status">Status</h2>
 <button v-bind:disabled="isDisabled">button</button>
  <h2 v-bind:class="isPromoted && 'promoted'">promoted</h2>
  <h2 v-bind:class="isSold?'sold':'new'"> Soldout? movie</h2>
  <h2 v-bind:class="['new','promoted']">new promoted movie</h2>
   <h2 v-bind:class="[isPromoted && 'promoted',isSold?'sold':'new']">array conditionality</h2>
  <h2 v-bind:class="{
    promoted: isPromoted,
    new:!isSold,
    'sold':isSold
    }">object conditionality</h2>
    <h2 v-bind:style="{
      color:'pink',
      'font-size': fontsize+px,
      padding:'20px'
      
      }">inline styles</h2>
      <h2 v-bind:style="style">object style binding</h2><!--v-bind:<attr>==:<attr>-->
     
 </div>
</template>

<script>
import ConditionalRendering from './components/ConditionalRendering.vue';


export default {
  components: { ConditionalRendering },
  name: 'App',
  data(){
    return{
      name:'Sai Charan',
      college:"NIT AP",
      htmlbinding:"<b>ECE</b>",
      headindID:'heading',
      isDisabled:true,
      status:'danger',
      isPromoted:true,
      isSold:true,
      fontsize:20,
      style:{
        fontSize:'30px',
        color:'yellow'
      }
    };
  },
  
};
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
.underline{
  text-decoration: underline;
}
.promoted
{
  font-style: italic;
}
.new{
  color: green;
}
.sold{
  color:red;
}
</style>
