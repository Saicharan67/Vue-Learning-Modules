<template lang="">
    <div>
        <div>Hello {{fullName}}</div>
        <button @click="sendEvent">Call Heroes</button>
    </div>
</template>
<script>
import {computed} from 'vue'
export default {
    name:"PersonGreeting",
    setup(props,context) {
        const fullName = computed(()=>{
            return `${props.firstName}${props.lastName}`
        })
        function sendEvent(){
            context.emit('callHeroes',fullName.value)
        }
        return{
            fullName,
            sendEvent
        }
    },
    props:['firstName','lastName']
}
</script>
<style lang="">
    
</style>