<template>
  <div id="app">
   <TopNavBar></TopNavBar>
   <div id="a"></div>
  </div>
</template>

<script>
import TopNavBar from './components/TopNavBar'
export default {
  name: 'App',
  components:{
    TopNavBar
  }
}
</script>

<style>
#a{
  height: 1000px;
  overflow: auto;
}
</style>
