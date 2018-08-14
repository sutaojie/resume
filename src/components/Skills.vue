<template>
    <section id="siteSkills" class="skills">
        <h2>技能</h2>
        <section class="tech-stack">
            <h3>前端</h3>
            <ul>

                <li v-for="skill in skills">
                    <div class="circle"></div>
                    <h4>{{skill.keyname}}</h4>
                    <ul>
                        <li v-for="list in skill.describe">{{list}}</li>
                    </ul>
                </li>
                
            </ul>
        </section>


    </section>
</template>

<script>
    export default{
        data(){
            return{
                skills:[
                    {
                        keyname:'ECMAScript（JavaScript）',
                        describe:[
                            '熟悉 ECMAScript，理解异步、单线程、this、作用域链、闭包、原型链、面向对象等。',
                            '了解 ES6 的部分常用语法,能在项目中普遍使用let、块级作用域、箭头函数、模板字符串、解构赋值、Promise 等语法。'
                            ]
                    },
                    {
                        keyname:'DOM/BOM',
                        describe:[
                            '熟悉 DOM 事件模型，捕获、冒泡以及如何阻止事件的传递。',
                            '熟悉原生 DOM 和 BOM 使用和相关标准。'
                        ]
                    },
                    {
                        keyname:'模块化与设计模式',
                        describe:[
                            '能使用 MVC 设计模式思想组织代码，使用模块化的编程思想进行开发。',
                            '了解 AMD 模块化思想进行代码模块化。',
                            '了解 CommonJS 配合 npm 以及构建工具进行基础的模块化操作。'
                        ]
                    },
                    {
                        keyname:'jQuery',
                        describe:[
                            '熟悉 jQuery 的常用 API，能使用 jQuery 技术栈进行网站开发。',
                            
                        ]
                    },
                    {
                        keyname:'Vue.js',
                        describe:[
                            '能使用 Vue.js 完成需求，了解 Vue.js 的数据双向绑定、数据响应式原理、父子组件间的通信原理。',
                            '能使用 Vue-Router 制作前端路由；能使用 vuex 进行状态管理。'
                        ]
                    },
                    {
                        keyname:'HTTP与浏览器',
                        describe:[
                            '了解 HTTP 基础知识，了解常见状态码含义，能够根据请求查看响应。',
                            '理解客户端缓存、同源策略，以及常用的跨域方法。',
                            '理解浏览器运行机制，理解页面加载的整个过程。'
                        ]
                    },
                    {
                        keyname:'Node.js',
                        describe:[
                            '了解 Node.js 的部分基础知识，使用过 Node.js 搭建简易服务器，使用过 express 框架做过 demo。'
                            ]
                    },
                    {
                        keyname:'命令行',
                        describe:[
                            '了解命令行，能够使用命令行进行常用的操作。'
                        ]
                    },
                    {
                        keyname:'Git',
                        describe:[
                            '了解 git 版本控制工具以及常用的操作。'
                        ]
                    },
                    {
                        keyname:'前端工程化',
                        describe:[
                            '使用过 WebPack 等前端打包工具，能够进行基础的使用。',
                            '能在项目中使用 Less / Sass 等预处理工具。',
                            '了解基本的前端安全，性能优化等知识，并能在项目中加以实践。'
                        ]
                    },
                    {
                        keyname:'HTML5 & CSS3',
                        describe:[
                            '标签语义化：能根据 HTML5 标准编写具有语义化的文档结构。',
                            'CSS居中与布局：能快速对元素进行居中处理，使用float、flex、grid等方案进行页面布局。',
                            'CSS动画：能使用keyframes、transition、transform等实现常见动画效果。',
                            '了解Bootstrap的基本使用规则。'
                        ]
                    },
                    {
                        keyname:'移动端页面',
                        describe:[
                            'PC 端能使用(meta name="viewport")以及媒体查询 (media query)进行响应式开发。',
                            '移动端根据百分比、动态 REM、vw/vh 等书写响应式页面，100% 还原设计稿。'
                        ]
                    }

                ]
            }
        }
    }
</script>

<style scoped>

section.skills,
section.portfolio {
  max-width: 940px;
  margin-left: auto;
  margin-right: auto;
  margin-top: 60px;
}
section.skills {
  background: #fff;
  padding: 50px 30px;
  box-shadow: 0px 1px 5px 0px rgba(0, 0, 0, 0.5);
  margin-bottom: 60px;
}
section.skills > h2,
section.message > h2,
section.portfolio > h2,
section.myPortfolio .section_header_title {
  color: #3d4451;
  font-size: 34px;
  line-height: 1.2;
  font-weight: 600;
  text-align: center;
}
section.skills .tech-stack > h3 {
  font-size: 19px;
  color: #574ABB;
  margin: 0 0 15px 5px;
  font-weight: bold;
}
section.skills .tech-stack h4 {
  line-height: 30px;
  font-size: 18px;
  font-weight: bold;
  bottom: 3px;
  color: #000;
}
section.skills .tech-stack > ul {
  border-left: 2px solid #7E6EFC;
  margin-left: 15px;
}
section.skills .tech-stack > ul > li {
  position: relative;
  top: -5px;
  margin: 0 0 20px 20px;
}
section.skills .tech-stack > ul > li li {
  line-height: 1.7;
  list-style: disc;
  margin-left: 2em;
}


.circle {
    /* display: none; */
  height: 14px;
  width: 14px;
  -webkit-border-radius: 100%;
  border-radius: 100%;
  background: #7E6EFC;
  float: left;
  position: absolute;
  left: -28px;
  top: 5px;
}
</style>
