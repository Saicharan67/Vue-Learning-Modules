<template lang="">
    <div>
        <h2> {{firstName}} {{lastName}} </h2>
    </div>
</template>
<script>
import {reactive,toRefs} from "vue"
export default {
    name:"DemoTwo",
    setup()
    {
        const state = reactive({
            firstName:"Sai",
            lastName:"Charan"
        })
        setTimeout(() => {
            state.firstName = "Xyz"
            state.lastName = "Abc"
        }, 2000);
        //By returning the values like below vue cant react to changes on them so we should toRefs method to solve this
        // return{
        //     firstName :state.firstName,
        //     lastName:state.lastName
        //}
        return toRefs(state)
    }
}
</script>
<style lang="">
    
</style>