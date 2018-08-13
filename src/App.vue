<template>
  <div id="app">
     <print></print>
   <top-nav-bar></top-nav-bar>
    <user-card ></user-card>
   <section class="myPortfolio"  id="siteWorks">
        <div class="boundary">
            <header class="section_header">
                <h2 class="section_header_title">项目经历</h2>
            </header>
            <works :works='workLists'></works>
        </div>
    </section>
    <skills></skills>
   
   
  </div>
</template>

<script>
import TopNavBar from './components/TopNavBar'
import UserCard from './components/UserCard'
import Works from './components/Works'
import Skills from './components/Skills'
import Print from './components/Print'
export default {
  name: 'App',
  data(){
    return{
      workLists:[
          {
            titles:{mainTitle:'多人共享博客' , subTitle:'- a Multi-user blog'},
            tags:['vue-cli', 'vue', 'axios', 'vue-router', 'vuex', 'es6', 'npm'],
            describe:'基于vue技术栈，做一款多人共享博客的单页应用，实现以下功能：',
            todos:['用户的登录、注册、注销功能。', '首页多人博客列表展示与用户博客列表展示。', '个人博客管理:创建、编辑、删除与发布。'],
            projectLinks:{view:'###', code:'#'},
            imgUrl:require('./assets/img/works/multi-user-blog.jpg'),
            imgDescribe:'导航栏'
          },
          {
            titles:{mainTitle:'在线简历编辑器', subTitle:'- a shareable resume-editor online'},
            tags:['HTML5', 'CSS3', 'JavaScript', 'Vue', 'LeanCloud'],
            describe:'基于vue技术栈，以LeanCloud为数据库，完成一个可分享的在线简历编辑器，实现以下功能：',
            todos:[' 用户的登录、注册、注销功能。', '信息区、技能区、项目区的可编辑功能。', '编辑器的保存、分享、打印、换肤功能。'],
            projectLinks:{view:'###', code:'#'},
            imgUrl:require('./assets/img/works/multi-user-blog.jpg'),
            imgDescribe:'简历编辑器'
          }
      ]
    }
  },
  components:{
    TopNavBar,
    UserCard,
    Works,
    Skills,
    Print,
    
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
