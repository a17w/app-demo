<template>
  <div id="app">
  <h1>{{ message }}</h1>
  <input v-model="message"/>
  <br/>
  <a v-bind:href="url">Click Me</a>
  <p v-if="show">Show Me</p>
  <p v-else="show">This is the else</p>
  <ul>
  <li v-for="item in items">
  {{item.test}}
  </li>
  </ul>
<button v-on:click="pressed">Press Me</button>
  </div>
</template>

<script>
export default {
  name: 'app',
  data () {
    return {
      message: 'Hello World from Annie',
      url: 'http://www.cnn.com',
      show: false,
      items: [ {test: 123}, {test: 456}, {test: 789} ]
    }
  },
  methods: {
    pressed () {
      alert('You Pressed Me!')
    }
  }
}
</script>

<style>
#app {
  font-family: 'Avenir', Helvetica, Arial, sans-serif;
  -webkit-font-smoothing: antialiased;
  -moz-osx-font-smoothing: grayscale;
  text-align: center;
  color: #2c3e50;
  margin-top: 60px;
}
</style>
