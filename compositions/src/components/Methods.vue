<template lang="">
    <div>
        <h2>{{count}}</h2>
        <button @click = "incrementCount">Increment count</button>

        <h2> {{firstName}} {{lastName}} </h2>
        <button @click="changeHeroName">Change HeroName</button>
    </div>
</template>
<script>
import { reactive ,ref, toRefs} from 'vue'
export default {
    name:"Methods",
    setup() {
        const count = ref(0)
        const state = reactive({
            firstName:"Bruce",
            lastName:"Wayne"
        })
        function incrementCount(){
            count.value+=1
        }
        function changeHeroName(){
            state.firstName = "Kent"
            state.lastName = "Clark"
        }
        return{
            count,
            ...toRefs(state),
            incrementCount,
            changeHeroName
        }
    }
}
</script>
<style lang="">
    
</style>