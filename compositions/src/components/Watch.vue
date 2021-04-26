<template lang="">
    <div>
        <input type='text' placeholder="Name" v-model="name"/>
        <input type='text' placeholder="Name" v-model="firstName"/>
        <input type='text' placeholder="reactiveName" v-model="fname"/>
  
    </div>
</template>
<script>
import { ref ,watch,reactive,toRefs} from 'vue'

export default {
    name:'Watch',
    setup() {
      const firstName = ref('') 
      const state = reactive({
          fname:'',

      })
      watch(firstName,(newValue,oldValue)=>{
           console.log({oldValue})
            console.log({newValue})
      })
      watch(()=>{
          return {...state}
      },(newValue,oldValue)=>{
          console.log(oldValue.fname)
          console.log(newValue.fname)
      })
      return{
          firstName,
            ...toRefs(state)

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