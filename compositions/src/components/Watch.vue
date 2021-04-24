<template lang="">
    <div>
        <input type='text' placeholder="Name" v-model="name"/>
        <input type='text' placeholder="Name" v-model="firstName"/>
    </div>
</template>
<script>
import { ref ,watch} from 'vue'

export default {
    name:'Watch',
    setup() {
      const firstName = ref('') 
      watch(firstName,(newValue,oldValue)=>{
           console.log({oldValue})
            console.log({newValue})
      })
      return{
          firstName
      } 
      
    },
    data()
    {
        return{
            name:'',
        }
    },
    watch:{
        name(newValue,oldValue){
            console.log({oldValue})
            console.log({newValue})
        }
    }
}
</script>
<style lang="">
    
</style>