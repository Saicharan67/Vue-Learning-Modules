<template>
    <div>
         <h2>{{ name }}</h2>
  <div>
    <button @click="changeName($event), increment(1, $event)">
      Change name
    </button>
  </div>
  <h2>{{ count }}</h2>
  <div>
    <button @click="increment(1, $event)">Increment</button>
    <button @click="decrement(1)">Decrement</button>
   
  </div>
    </div>
</template>
<script>


export default {
    name:'EventHandling',
    data() {
        return{
            name:'saicharan'
        }
     
    },
}
</script>
<style>

</style>