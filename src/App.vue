<template>
  <div id="app">
   <TopNavBar></TopNavBar>
    <div class="blank"></div>
    <UserCard></UserCard>
   <section class="myPortfolio"  id="siteWorks">
        <div class="boundary">
            <header class="section_header">
                <h2 class="section_header_title">项目经历</h2>
            </header>
            <Works></Works>
        </div>
    </section>
  </div>
</template>

<script>
import TopNavBar from './components/TopNavBar'
import UserCard from './components/UserCard'
import Works from './components/Works'
export default {
  name: 'App',
  data(){
    return{
      workLists:[

      ]
    }
  },
  components:{
    TopNavBar,
    UserCard,
    Works
  }
}
</script>

<style>


section.myPortfolio {
  margin-top: 180px;
  background: #fff;
  padding: 60px 0 60px 0;
}
.boundary {
   
  clear: both;
  padding: 50px 0;
  width: 940px;
  margin: 0 auto;
}
.boundary .section_header {
  text-shadow: 1px 1px 0 #fff;
  line-height: 1.4;
}
.boundary .section_header .section_header_title {
  margin-bottom: 32px;
}

section.myPortfolio .section_header_title {
  color: #3d4451;
  font-size: 34px;
  line-height: 1.2;
  font-weight: 600;
  text-align: center;
}
</style>
