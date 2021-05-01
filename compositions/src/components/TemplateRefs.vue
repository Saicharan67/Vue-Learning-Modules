<template lang="">
    <div>
        <input type="text" ref="inputRef"/>
    </div>
</template>
<script>
import {onMounted, ref} from 'vue'
export default {
    name:"templateRef",
    setup() {
        const inputRef = ref(null)
        onMounted(()=>{
            inputRef.value.focus( )
        })
           return{
        inputRef
    }
    },
 
}
</script>
<style lang="">
    
</style>