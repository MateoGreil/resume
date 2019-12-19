<template>
  <div id="app" v-bind:style="{ backgroundColor: color}">
    <img alt="Vue logo" src="./assets/logo.png">
    <HelloWorld/>
  </div>
</template>

<script>
import HelloWorld from './components/HelloWorld.vue'

export default {
  name: 'app',
  components: {
    HelloWorld
  },
  data () {
    console.log(10000 - window.innerHeight)
    return {
      scrollYMax: 10000 - window.innerHeight,
      shiftY: 255 / (10000 - window.innerHeight),
      color: 'rgb(255, 255, 255)'
    }
  },
  methods: {
    handleScroll () {
      var color = (this.shiftY * (this.scrollYMax - scrollY)).toFixed().toString()
      this.color = 'rgb(' + color + ', ' + color + ', ' + color + ')'
      console.log(color)
    }
  },
  created () {
    window.addEventListener('scroll', this.handleScroll)
  },
  destroyed () {
    window.removeEventListener('scroll', this.handleScroll)
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
  height: 20000px;
}
</style>
