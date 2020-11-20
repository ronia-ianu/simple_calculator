<template>
<h1>Simple calculator</h1>
<p>
<label for="number1">Number 1:</label><input name="number1" v-model.number="number1" type="number">
</p>
<p>
<label for="number2">Number 2:</label><input name="number2" v-model.number="number2" type="number">
</p>
<button v-on:click="add">Add</button>
<button v-on:click="subtract">Subtract</button>

<!-- 
  TODO
  Add the buttons for multiplication and division here
 -->
<button v-on:click="multiply">Multiply</button>
<button v-on:click="divide">Divide</button>


<!-- End TODO -->
<p>
<label for="result">Result:</label><input name="result" v-model.number="result" readonly type="number">
</p>
</template>

<script>
export default {
  name: 'App',
  data () {
    return {
      number1: 0,
      number2: 0,
      result: 0
    }
  },
  methods: {
    add () {
      this.result = this.number1 + this.number2
    },
    subtract () {
      this.result = this.number1 - this.number2
    },
    /*
      TODO

      Add the functions for multiplication and division here
    */
    
    multiply () {
      this.result = this.number1 * this.number2
    },
    divide () {
      this.result = this.number1 / this.number2
    },
    /*
      End TODO
    */
  }
}
</script>

<style>
#app {
  font-family: Avenir, Helvetica, Arial, sans-serif;
  text-align: center;
  color: #2c3e50;
}

label {
  margin: 3px;
  width: 100px;
  display: inline-block;
  text-align: end;
}

input {
  margin: 3px;
  width: 200px;
}
button {
  margin: 3px;
}
</style>
