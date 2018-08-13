<template>
    <div class="section_body">
                <section class="project">
                    <div class="project_intro">
                        <header class="project_intro_header clearfix">
                            <h4 class="project_intro_header_title">多人共享博客<span> - a Multi-user blog</span></h4>
                            <ul class="tech-tag-list">
                                <li class="tech-tag-list_item tech-tag-list_item-vue-cli">vue-cli</li>
                                <li class="tech-tag-list_item tech-tag-list_item-vue">vue2</li>
                                <li class="tech-tag-list_item tech-tag-list_item-axios">axios</li>
                                <li class="tech-tag-list_item tech-tag-list_item-vue-router">vue-router</li>
                                <li class="tech-tag-list_item tech-tag-list_item-vuex">vuex</li>
                                <li class="tech-tag-list_item tech-tag-list_item-es6">es6</li>
                                <li class="tech-tag-list_item tech-tag-list_item-npm">npm</li>
                                <!--<li class="tech-tag-list_item tech-tag-list_item-jQuery">jQuery</li>-->

                            </ul>
                        </header>
                        <div class="project_intro_header_content">
                            <p>
                                基于vue技术栈，做一款多人共享博客的单页应用，实现以下功能：
                            </p>
                            <ul class="list">
                                <li>用户的登录、注册、注销功能。</li>
                                <li>首页多人博客列表展示与用户博客列表展示。</li>
                                <li>个人博客管理:创建、编辑、删除与发布。</li>
                            </ul>
                            <p class="project_intro_links">
                                <a href="https://littlebirdflying.github.io/multi-user-blog/dist/#/" target="_blank">预览地址</a>
                                <a href="https://github.com/littlebirdflying/multi-user-blog" target="_blank">源码地址</a>
                            </p>
                        </div>
                    </div>
                    <div class="project_thumb">
                        <img :src="imgUrl" alt="导航栏">
                    </div>
                </section>
                <!--  -->
            </div>
</template>

<script>
    export default{
        data(){
            return{
                imgUrl:''
            }
        },
        created(){
            this.imgUrl=require('../assets/img/works/multi-user-blog.jpg')
        }
    }
</script>

<style>

.boundary .section_body .project {
  border-top: 2px dashed #ccc;
  display: flex;
  justify-content: space-between;
  margin-top: 25px;
  padding-top: 35px;
}
.boundary .section_body .project .project_intro {
  width: 60%;
  padding: 0 10px 0 0;
}
.boundary .section_body .project .project_intro .project_intro_header {
  position: relative;
  margin-bottom: 8px;
  line-height: 1.3;
}
.boundary .section_body .project .project_intro .project_intro_header .project_intro_header_title {
  font-size: 1.2em;
  font-weight: bold;
  padding-bottom: 3px;
}
.boundary .section_body .project .project_intro .project_intro_header .project_intro_header_title span {
  font-size: 16px;
  font-style: italic;
}
.boundary .section_body .project .project_intro .project_intro_header .tech-tag-list .tech-tag-list_item {
  height: 24px;
  line-height: 24px;
  padding: 0 6px;
  border-radius: 3px;
  display: inline-block;
  vertical-align: middle;
  font-size: 0.75em;
  font-family: 'Lucida Grande', arial;
  color: #fff;
}
.boundary .section_body .project .project_intro .project_intro_header_content {
  line-height: 1.7;
  text-align: justify;
}
.boundary .section_body .project .project_intro .project_intro_header_content ul {
  list-style: inherit;
  margin-left: 1.3em;
}
.boundary .section_body .project .project_intro .project_intro_header_content .project_intro_links {
  margin-top: 10px;
  text-align: right;
  word-spacing: 1em;
}
.boundary .section_body .project .project_intro .project_intro_header_content .project_intro_links > a,
.boundary .section_body .project .project_intro .project_intro_header_content .project_intro_links > a:visited {
  color: #08c;
}
.boundary .section_body .project .project_intro .project_intro_header_content .project_intro_links > a:hover {
  text-decoration: underline;
}
.boundary .section_body .project .project_thumb {
  background: #eee;
  width: 38%;
}
section.message > ol {
  max-width: 700px;
  margin: 0 auto;
  border-top: 1px solid #DDD;
}
section.message > ol > li {
  padding: 16px;
  border-bottom: 1px solid #DDD;
}



.tech-tag-list_item-html {
  background: #f60;
}
.tech-tag-list_item-css {
  background: #f90;
}
.tech-tag-list_item-javascript {
  background: #ffda3f;
  color: #333 !important;
}
.tech-tag-list_item-nodejs {
  background: #80bd01;
}
.tech-tag-list_item-jQuery {
  background: #015a84;
}
.tech-tag-list_item-vue {
  background: #80bd01;
}
.tech-tag-list_item-vue-cli {
  background: #8f94dc;
}
.tech-tag-list_item-axios {
  background: #97a0ad;
}
.tech-tag-list_item-vue-router {
  background: #d7a273;
}
.tech-tag-list_item-vuex {
  background: #92c3cb;
}
.tech-tag-list_item-es6 {
  background: #687772;
}
.tech-tag-list_item-npm {
  background: #f5a573;
}
.tech-tag-list_item-lean-cloud {
  background: #3b4f40;
}
.tech-tag-list_item-qiniu {
  color: #333 !important;
  background: #ebe3df;
}
</style>
