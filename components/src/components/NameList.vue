<template >
    <div>
        <h3 v-for="name in names" :key="name.firstName">
           <slot :firstName="name.firstName" :lastName="name.lastNmae"></slot>
        </h3>
    </div>
</template>
<script>
export default {
    name:'NameList',
   data(){
       return{
            names:[
                {
                    firstName: 'b',
                    lastNmae: 'w'
                },
                  {
                    firstName: 'b',
                    lastNmae: 'w'
                },
                  {
                    firstName: 'b',
                    lastNmae: 'w'
                },
            ]
   }
}
}
</script>
<style lang="">
    
</style>