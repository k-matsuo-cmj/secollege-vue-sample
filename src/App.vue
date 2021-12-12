<template>
<p>
  <img alt="Vue logo" src="./assets/logo.png">
  <Hello name="田中" />
  <NameList />
</p>
</template>

<script>
import Hello from './components/Hello.vue'
import NameList from './components/NameList.vue'

export default {
  name: 'App',
  components: {
    Hello,
    NameList
  }
}
</script>

<style>
#app {
  font-family: Avenir, Helvetica, Arial, sans-serif;
  -webkit-font-smoothing: antialiased;
  -moz-osx-font-smoothing: grayscale;
  text-align: center;
  color: #2c3e50;
  margin-top: 60px;
}
</style>
