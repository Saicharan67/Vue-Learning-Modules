<template>
    <div>
        <h2 v-bind:key="index" v-for="(name,index) in names">{{index}}  {{name}}</h2>
        <h2 :key="name" v-for="name in fullnames">{{name.first}} {{name.last}}</h2>
    </div>
</template>
<script>


export default {
    data() {
        return{
            names:['sai','charan','mahankali'],
            fullnames:[
                {first:'ross',last:'geller'},
                {first:'joe',last:'trib'},
                {first:'bing',last:'chandler'},
            ]
        }
    },
}
</script>
<style>

</style>