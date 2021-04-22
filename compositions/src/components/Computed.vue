<template lang="">
    <div> 
        <input type="text" placeholder="First Name" v-model="fName"/>
        <input type="text" placeholder="Last Name" v-model="lName"/>
        <h3>Options FullName is {{fullName}}</h3>
        <input type="text" placeholder="First Name" v-model="refFirstName"/>
        <input type="text" placeholder="Last Name" v-model="refLastName"/>
        <h3>Compositions FullName is {{refFullName}}</h3>
        <input type="text" placeholder="First Name" v-model="reactiveFirstName"/>
        <input type="text" placeholder="Last Name" v-model="reactiveLastName"/>
        <h3>Reactive FullName is {{reactiveFullName}}</h3>

    </div>
</template>
<script>
import {ref,computed,reactive,toRefs} from 'vue'
export default {
    name:'Computed',
    setup() {
      const  refFirstName = ref('')
      const refLastName = ref('')
      const state = reactive({
          reactiveFirstName:'',
          reactiveLastName:''
      })
      const refFullName =  computed(function(){
          return `${refFirstName.value}${refLastName.value}`
      })
      const reactiveFullName = computed(()=>{
          return `${state.reactiveFirstName}${state.reactiveLastName}`
      })
      return{
          refFirstName,
          refLastName,
          refFullName,
          reactiveFullName,
          ...toRefs(state)
      }

    },
     data(){
        return{
            fName:'',
            lName:''
        }
    },
    computed:{
        fullName(){
            return `${this.fName}${this.lName}`
        }
    }
}
</script>
<style lang="">
    
</style>