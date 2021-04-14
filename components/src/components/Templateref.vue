<template lang="">
    <div>
        <input type='text' ref="inputfocus"/>
    </div>
</template>
<script>
// if ref attr is used on plain dom elment the reference will be that elemnt and if the ref attr is used on child component the reference will be the component instance  
export default {
    name: "Templateref",
    mounted(){
        this.$refs.inputfocus.focus()
    }
}
</script>
<style lang="">
    
</style>