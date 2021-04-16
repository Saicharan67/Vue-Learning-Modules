<template lang="">
  <div>
    <h2>Options - {{ o_firstName }}</h2>
    <h2>Options - {{ o_firstName }} {{o_LastName}} a k a {{o_heroName}} </h2>
    <h2>Compositions - {{ c_firstName }}</h2>
    <h2>Compositions - {{ c_firstName }} {{c_lastName}} a k a {{c_heroName}} </h2>
    <h2>Reactive Compositions - {{state.firstName}} {{state.lastName}} a k a {{state.heroName}}
  </div>
</template>
<script>
import { ref , reactive} from "vue";
export default {
  name: "Data",
  setup() {
    
    //ref returns  a reactive and immutable  reference to the internal value its holding and we can use it by .value
    const c_firstName = ref("Clark");
    const c_lastName = ref("kent")
    const c_heroName = ref("SuperMan")
    console.log({ c_firstName });

    const state = reactive({
      firstName: "Princess",
      lastName: "Diana",
      heroName: "Wonder Women"
    });

    return {
      c_firstName,
      c_lastName,
      c_heroName,
      state
    };
  },
  data() {

    return {
      o_firstName: "Bruce",
      o_LastName: "Wayne",
      o_heroName:"BatMan"
    };
  },
};
</script>
<style lang=""></style>
