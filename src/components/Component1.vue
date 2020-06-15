<template>
  <div class="main-area">
    <div class="square" 
        @mouseover='addBlue = !addBlue'
        @click='addRed = !addRed'
        :class='divClasses'>
    </div>
    <div class="square" :class='color'></div>
    <div class="square" :class='[color, {red: this.addRed}]'></div> 
    <hr>
    <input type='text' v-model='color'/>
    <hr>
    <div class="square" :style='newStyle'></div>
    <input type='text' v-model='color2'/>
    <input type='text' v-model='width'/>
  </div>
</template>

<script>
export default {
  name: 'Component1',
  data: function () {
    return {
      addRed: true,
      addBlue: false,
      color: 'green',
      color2: 'gray',
      width: 300
    }
  },
  computed: {
    divClasses: function () {
      return {
        red: this.addRed,
        blue: !this.addBlue
      }
    },
    newStyle: function () {
      return{
        backgroundColor: this.color2,
        width: this.width + 'px'
      }
    }
  }
}
</script>

<!-- Add "scoped" attribute to limit SS to this component only -->
<style scoped>
  .main-area {
    text-align: center;
  }
  .square {
    height: 300px;
    width: 300px;
    display: inline-block;
    background-color: grey;
    margin: 10px;
  }

  .red {
    background-color: red;
  }

  .blue {
    background-color: blue;
  }

  .green {
    background-color: green;
  }
</style>
