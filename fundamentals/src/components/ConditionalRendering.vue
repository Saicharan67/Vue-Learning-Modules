<template>
<div>
      <h2 v-if="num === 0">num is zero</h2>
      <h2 v-else-if="num<0">The number is negative</h2>
      <h2 v-else-if="num>0">The number is positive</h2>
      <h2 v-else>Not a number</h2>
      <template v-if="display">
         <h2>Saicharan</h2>
        <h2>ConditionalRendering</h2>
        <h2>Vue</h2>
      </template>
      <h2 v-show="show">using v-show</h2>
       <h2 v-if="show">using v-if</h2>
      
      
</div>
  
</template>
<script>


export default {
    name:'conditional',
    data() {
        return{
            num:'@',
            display:true,
            show:false
        }
    },
}
</script>
<style >

</style>