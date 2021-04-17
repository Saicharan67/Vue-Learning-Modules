<template lang="">
    <div>
        <h2> {{name}} </h2>
    </div>
</template>
<script>
import {ref } from "vue"
export default {
    name:"DemoOne",
    setup(){
        //let name1 = "mahankali"
        //By returing a const or let value vue doesnt know how to react to change in values so we use reactive or refs for that
        let name = ref("Charan")
        setTimeout(() => {
            name.value = "Sai"
            //name1 = "xyz"
        }, 2000);
        return{
            //name1
            name
        }
    }
}
</script>
<style lang="">
    
</style>