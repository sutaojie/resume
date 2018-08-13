<template>
  <div id="app">
   <TopNavBar></TopNavBar>
    <UserCard></UserCard>
   
  </div>
</template>

<script>
import TopNavBar from './components/TopNavBar'
import UserCard from './components/UserCard'
export default {
  name: 'App',
  components:{
    TopNavBar,
    UserCard
  }
}
</script>

<style>
#a{
  height: 1000px;
  overflow: auto;
}
</style>
