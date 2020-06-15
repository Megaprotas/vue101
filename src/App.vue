<template>
  <div id="app">
    <Component3/>
    <Component2/>
    <Component1/>
  </div>
</template>

<script>
import Component1 from './components/Component1.vue'
import Component2 from './components/Component2.vue'
import Component3 from './components/Component3.vue'

export default {
  name: 'App',
  components: {
    Component1,
    Component2,
    Component3,
  }
}
</script>

<style>
#app {
  
}
</style>
