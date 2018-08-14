<template>
     <div id="topNavBar" class='topNavBar '  :class='{sticky:scrolled, notPrint:isPrinting}' @scroll="handleScroll" >
        <div class="topNavBar-inner clearfix">
            <a class="logo" href="#" alt="logo" style="float:left;" v-for="item in logo">
                <span :class="item.cls">{{item.chart}}</span>
            </a>
            <nav class="menu">
                <ul class="clearfix">
                    <li v-for="list in menuList"><a :href="list.link">{{list.keyword}}</a></li>
                    
                </ul>
            </nav>
        </div>

    </div>
</template>

<script>
    import '../assets/common/common.css'
    import '../assets/common/print.css'
    import eventhub from '../assets/common/evenhub.js'
    export default{
        name:'topNavBar',
        data(){
            return {
                scrolled:false,
                logo:[{ cls:'rs', chart:'S' }, { cls:'card', chart:'ZY' }],
                menuList:[
                    {link:'#siteAbout', keyword:'关于'},
                    {link:'#siteWorks', keyword:'作品'},
                    {link:'#siteSkills', keyword:'技能'},
                    // {link:'#blog', keyword:'博客'},
                ],
                isPrinting:false
            }
        },
        created(){
           window.addEventListener('scroll', this.handleScroll);

              eventhub.$on('isprint',function(e){
                   this.isPrinting = e
                console.log(typeof this.isPrinting);
                alert(this.isPrinting)
              })
            
        },
        mounted(){

        },
        methods:{
           handleScroll(){
                this.scrolled = window.scrollY > 0;
               }
  
        },
        computed:{
           
        },
        watch:{
           
        },
    }
</script>

<style scoped>
.notPrint {
    display:none;
}

.topNavBar {
  padding: 20px 0 20px 0;
  position: fixed;
  top: 0;
  left: 0;
  width: 100%;
  transition: all 0.5s;
  z-index: 1;
  color: #B7B7B7;
}
.topNavBar.sticky {
  background: white;
  padding: 10px 0;
  box-shadow: 0 0 10px rgba(0, 0, 0, 0.25);
  color: #3d4451;
}
.topNavBar-inner {
  padding: 0 16px;
  /*display:flex;*/
  /*flex-direction: column;*/
  /*align-items: center;*/
}
.topNavBar-inner .menu {
  float: right;
}
.topNavBar-inner .logo {
  float: left;
}
.topNavBar nav {
  padding-top: 5px;
}
.topNavBar nav > ul {
  list-style: none;
  margin: 0;
  padding: 0;
}
.topNavBar nav > ul > li {
  float: left;
  margin-left: 30px;
  margin-right: 30px;
  position: relative;
}
.topNavBar nav > ul > li a {
  font-size: 18px;
  color: inherit;
  text-decoration: none;
  font-weight: bold;
  border-top: 3px solid transparent;
  border-bottom: 3px solid transparent;
  padding-top: 5px;
  padding-bottom: 5px;
  display: block;
  position: relative;
}
.topNavBar nav > ul > li.active > a::after,
.topNavBar nav > ul > li.highlight > a::after {
  content: '';
  display: inline-block;
  position: absolute;
  top: 100%;
  left: 0;
  width: 100%;
  background: rgb(252, 110, 146);
  height: 3px;
  animation: menuSlide 0.3s;
}
@keyframes menuSlide {
  0% {
    width: 0;
  }
  100% {
    width: 100%;
  }
}
.topNavBar .submenu {
  display: none;
  position: absolute;
  right: 0;
  top: 100%;
  background: white;
  color: #3d4451;
  box-shadow: 0 0 5px rgba(0, 0, 0, 0.5);
  cursor: pointer;
}
.topNavBar li.active > .submenu {
  display: block;
  animation: submenuSlide 0.3s;
}
@keyframes submenuSlide {
  0% {
    margin-right: 100%;
    /*自己多试试别的属性*/
  }
  100% {
    margin-right: 0%;
  }
}
.topNavBar .submenu > li {
  white-space: nowrap;
  padding: 5px 10px;
}
.topNavBar .logo {
  font-size: 24px;
  font-family: "Arial Black";
  padding-top: 3px;
  padding-bottom: 4px;
}
.topNavBar .logo .rs {
  color: rgb(252, 110, 146);
}
.topNavBar .logo .card {
  color: #9a9da2;
}
</style>
