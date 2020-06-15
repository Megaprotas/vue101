<template>
  <div class="main-area">
    <p v-if='show'>Some text</p>
    <p v-else>Meh</p>
    <button @click='show = !show'>Toggle</button>
    <hr>

    <div>
        <ul>
            <li v-for='(some, index) in someArray' :key='some.idx'> {{ some }} ({{ index }})</li>
        </ul>
        <ul>
            <li v-for='(name, index) in names' :key='name.id'>{{ name.title }} {{ name.id }} ({{ index }})</li>
        </ul>
        <span v-for='i in 10' :key='i.id'> {{ i }}</span>
    </div>
  </div>
</template>

<script>
export default {
  name: 'Component2',
  data: function () {
    return {
      show: true,
      someArray: ['Aaaa', 'Bv', 'Caas'],
      names: [
            {title: 'EJ', id: 1},
            {title:'AK', id: 2},
            {title: 'MJ', id: 3}
      ]
    }
  },
  methods: {
    toggleMethod: function () {
        return {

        }
    }
  }
}
</script>

<!-- Add "scoped" attribute to limit CSS to this component only -->
<style scoped>
</style>