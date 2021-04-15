<template lang="">
    <div>
        <h2>Options - {{o_firstName}}</h2>
        <h2>Compositions - {{c_firstName}}</h2>
    </div>
</template>
<script>
import {ref} from 'vue'
export default {
    name: 'Data',
    setup() {
        const c_firstName = ref('Charan')
        console.log({c_firstName})
        return{
            c_firstName
        }
    },
    data(){
        return{
            o_firstName:"Sai"
        }
    }
}
</script>
<style lang="">
    
</style>