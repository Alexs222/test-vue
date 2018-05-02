<template lang="pug">
  #app
    test-comp(
      title="Hello from test!"
      @buttonWasClicked="handleEmit"
    )
      .one(slot='top')
        h1 top
      .two(slot='bottom')
        h3 bottom
      .other
        h5 default
</template>


<script>
import testComponent from './components/test'
export default {
  components: {
    testComp: testComponent
  },
  name: 'app',
  data () {
    return {
      msg: 'Welcome to Your Vue.js App'
    }
  },
  methods: {
    handleEmit(name, counter, isActive) {
      console.log(name, counter, isActive);
      
    }
  }
}
</script>

<style lang="scss">
#app {
  font-family: 'Avenir', Helvetica, Arial, sans-serif;
  -webkit-font-smoothing: antialiased;
  -moz-osx-font-smoothing: grayscale;
  text-align: center;
  color: #2c3e50;
  margin-top: 60px;
}

h1, h2 {
  font-weight: normal;
}

ul {
  list-style-type: none;
  padding: 0;
}

li {
  display: inline-block;
  margin: 0 10px;
}

a {
  color: #42b983;
}
</style>
