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
            titles:{mainTitle:'优品商城' , subTitle:'- a mobile phone goods-shop'},
            tags:['Vue', 'Vuex', 'Vue-router', 'Vue-cli', 'javascript', 'npm'],
            describe:'基于Vue + Vue-router + Vuex技术栈，使用 Mock 数据来重构商城的项目，实现以下功能：',
            todos:['展示商品列表、展示热门商品、展示商品详情。', '购物车的购买，删除等操作。', '个人地址的管理及路由的跳转等'],
            projectLinks:{view:'#', code:'https://github.com/sutaojie/U-zhan-1/'},
            imgUrl:require('./assets/img/works/shop.jpg'),
            imgDescribe:'优品商城'
          },
          {
            titles:{mainTitle:'网易云播放器' , subTitle:'- a Netease cloud player'},
            tags:['jQuery', 'html5', 'css3', 'javascript', 'leancloud', 'qiniu', 'npm'],
            describe:'基于jQuery技术栈，以LeanCloud和QiNiu为数据库，完成一个移动端网易云播放器，实现以下功能：',
            todos:['展示歌曲列表、展示热歌榜歌曲、搜索歌曲。', '歌曲播放、暂停、歌词展示。', '搭建后台管理系统，实现歌曲新建、添加、编辑、删除。'],
            projectLinks:{view:'https://sutaojie.github.io/163music/src/index.html', code:'https://github.com/sutaojie/163music/tree/master/src/'},
            imgUrl:require('./assets/img/works/music.jpg'),
            imgDescribe:'网易云播放器'
          },
          {
            titles:{mainTitle:'小黄人', subTitle:'- code a Minion for you'},
            tags:['HTML5', 'CSS3', 'JavaScript', 'jQuery'],
            describe:'基于 jQuery，动态向 style 标签添加样式以及 pre 标签添加文本，模拟css绘制小黄人的过程，主要功能有：',
            todos:[' 同时显示style代码和绘画过程。', '增加播放代码速度调节按钮。', '适配手机端。'],
            projectLinks:{view:'https://sutaojie.github.io/cartoon/index.html', code:'https://github.com/sutaojie/cartoon'},
            imgUrl:require('./assets/img/works/Minion.jpg'),
            imgDescribe:'小黄人'
          },
          {
            titles:{mainTitle:'快捷导航', subTitle:'-a Quick Navigation Page'},
            tags:['HTML5', 'CSS3', 'JavaScript'],
            describe:'基于原生 JavaScript 结合 localStorage 在线存储功能，动态生成一个优美快捷的个人导航页。实现以下功能：',
            todos:[' 键盘快捷导航功能,敲击键盘字母跳转到绑定导航网址。', '导航键编辑导航地址功能。', '主流搜索引擎搜索功能。'],
            projectLinks:{view:'https://sutaojie.github.io/navigator-demo/index.html', code:'https://github.com/sutaojie/navigator-demo'},
            imgUrl:require('./assets/img/works/nav-page.jpg'),
            imgDescribe:'快捷导航'
          },
          {
            titles:{mainTitle:'会动的简历', subTitle:'- make your resume active'},
            tags:['HTML5', 'CSS3', 'JavaScript'],
            describe:'基于原生 JavaScript 和 CCS 3，动态向 style 标签添加样式以及 pre 标签添加文本，利用 prism.js 实现代码高亮,使简历生动起来。',
            todos:[],
            projectLinks:{view:'https://sutaojie.github.io/play-resume/index.html', code:'https://github.com/sutaojie/play-resume'},
            imgUrl:require('./assets/img/works/animation-resume.jpg'),
            imgDescribe:'会动的简历'
          },
           {
            titles:{mainTitle:'smart 在线画板', subTitle:'- Draw anything your want'},
            tags:['HTML5', 'CSS3', 'JavaScript'],
            describe:'基于原生 JavaScript 与 canvas 实现的在线画板，主要功能有：',
            todos:['实现任意选择颜色、画笔类型以及擦除等绘画功能。', '实现在线画板的本地保存功能。', '支持手机在线绘画功能。'],
            projectLinks:{view:'https://sutaojie.github.io/canvas-demo/index.html', code:'https://github.com/sutaojie/canvas-demo'},
            imgUrl:require('./assets/img/works/canvas.jpg'),
            imgDescribe:'在线画板'
          },
      ],
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

<style scoped>


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
