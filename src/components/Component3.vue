<template>
  <div class="main-area">
    <p :style='extraFn' :class='extraFn'> {{ number }} </p>
    <button @click='addition'>Add</button>
    <button @click='deduction'>Deduct</button>
  </div>
</template>

<script>
export default {
  name: 'Component3',
  data: function () {
    return {
      number: 0,
    }
  },
  methods: {
    addition: function () {
        var othernumber = this.rounding(2, 8);
        this.number += othernumber;

    },
    deduction: function () {
        var othernumber = this.rounding(4, 6);
        this.number -= othernumber;
    },
    rounding: function(min, max) {
        return Math.max(Math.floor(Math.random() * max) + 1, min);
    },
  }
}
</script>

<!-- Add "scoped" attribute to limit CSS to this component only -->
<style scoped>
    .red {
        background-color: red;
        color: red;
    }
</style>