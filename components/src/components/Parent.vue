<template>
  <div>
    Parent component
    <button @click="showChild = !showChild">Toggle Child</button>
    <child v-if="showChild" />
  </div>
</template>

<script>
import child from './child'
export default {
  components: { child },
  name: 'Parent',
  data() {
    return {
      showChild: true,
    }
  },
  beforeCreate() {
    console.log('Parent beforeCreate()')
  },
  created() {
    console.log('Parent created()')
  },
  beforeMount() {
    console.log('Parent beforeMount()')
  },
  mounted() {
    console.log('Parent mounted()')
  },
  beforeUpdate() {
    console.log('Parent beforeUpdate()')
  },
  updated() {
    console.log('Parent updated()')
  },
  beforeUnmount() {
    console.log('Parent beforeUnmount()')
  },
  unmounted() {
    console.log('Parent unmounted()')
  },
}
</script>

<style scoped>
</style>