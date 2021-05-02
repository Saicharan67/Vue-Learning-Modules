<template lang="">
    <div>
        <button @click="incrementCount">Clicked {{count}} times</button>
    </div>
</template>
<script>
//import counter from '../mixins/counter'
import useCounter from '../composables/useCounter'
export default {
    name:'ClickCounter',
   // mixins:[counter]
   setup(props) {
       const  {incrementCount , incrementCount}= useCounter(100,10)
       return{
           count,
           incrementCount
       }
   }
}
</script>
<style lang="">
    
</style>