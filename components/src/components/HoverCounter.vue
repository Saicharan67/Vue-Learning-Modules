<template lang="">
    <div>
        <h3 @mouseover="incrementCounter">Hovered {{count}} times</h3>
    </div>
</template>
<script>
import CounterMixin from '../mixins/counter.js'
export default {
    name:'HoverCounter',
    mixins:[CounterMixin]
}
</script>
<style lang="">
    
</style>