<template>
  <div id="app">
    <img src="./assets/logo.png">
    <HelloWorld3 msgFromFather='my-home'></HelloWorld3> 
   <HelloWorld4 msgFromFather='my-home'></HelloWorld4>

  </div>
</template>

<script>
import HelloWorld3 from './components/HelloWorld'
 import HelloWorld4 from './vue/todolist'
 
export default {
    // name: 'App5',
    name: 'App',
  components: {
    HelloWorld3,
     HelloWorld4
  },
   data () {
    return {
      msg: 'Welcome to Your Vue.js App',
      aaa: 'abcdefg'
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
