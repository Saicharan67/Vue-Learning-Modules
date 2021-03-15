<template lang="">
    <div>
        <h2>Fullname - {{ firstName }} {{ lastName }}</h2>
  <h2>Fullname - {{ fullName }}</h2>
  <h2>
    Total - {{ items.reduce((total, curr) => (total = total + curr.price), 0) }}
  </h2>
  <h2>Computed Total - {{ total }}</h2>
  <h2>Method Total - {{ getTotal() }}</h2>
  <button @click="items.push({ id: 4, title: 'Keyboard', price: 50 })">
    Add item
  </button>
  <div>
    <input type="text" v-model="country" />
  </div>
  <template v-for="item in items" :key="item.id">
    <h2 v-if="item.id === 1">{{ item.title }} - {{ item.price }}</h2>
  </template>
  <h2 v-for="item in expensiveItems" :key="item.id">
    {{ item.title }} - {{ item.price }}
  </h2>
  <button @click="changeFullName">Change fullname</button>

    </div>
</template>
<script>
export default {
    name:'computedprops',
    data(){
        return{
            lastName:'sai',
            firstName:'charan'
        }
    }
    computed: {
    fullName: {
      get() {
        return `${this.firstName} ${this.lastName}`
      },
      set(value) {
        const names = value.split(' ')
        this.firstName = names[0]
        this.lastName = names[1]
      },
    },
    total() {
      console.log('total computed property')
      return this.items.reduce((total, curr) => (total = total + curr.price), 0)
    },
    expensiveItems() {
      return this.items.filter((item) => item.price > 100)
    },
  },
}
</script>
<style lang="">
    
</style>