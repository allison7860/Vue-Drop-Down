<template>
  <div id="app">
    <router-view/>
  </div>
</template>

<script>
import List from './components/List'
export default {
  name: 'App',
	components: { //sub components
	List }
}
</script>

<style>
body {
margin:0;
background:#2e2d33;
}
#app {
  font-family: 'Century Gothic', sans-serif;
  -webkit-font-smoothing: antialiased;
  -moz-osx-font-smoothing: grayscale;
  color: #fff;
}
</style>
