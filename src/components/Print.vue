<template>
    <div>
     <div class="personal-info-print" style="display:none">
            <h1 class="name">苏赵勇</h1>
            <p class="description">男，1995/11，大专(2014-2017)，安徽财贸大学，自学前端一年。</p>
            <ul class="contact">
                <li>
                    <svg class="icon" aria-hidden="true">
                        <use xlink:href="#icon-shouji"></use>
                    </svg>
                    17682488600
                </li>
                <li>
                    <svg class="icon" aria-hidden="true">
                        <use xlink:href="#icon-QQ"></use>
                    </svg>
                    1522006120
                </li>
                <li>
                    <svg class="icon" aria-hidden="true">
                        <use xlink:href="#icon-weixin"></use>
                    </svg>
                    Coco-6120
                </li>
                <li>
                    <svg class="icon" aria-hidden="true">
                        <use xlink:href="#icon-youxiang"></use>
                    </svg>
                    sutaojie@163.com
                </li>
                <li>
                    <svg class="icon" aria-hidden="true">
                        <use xlink:href="#icon-blogger"></use>
                    </svg>
                    https://sutaojie.github.io/
                </li>
                <li>
                    <svg class="icon" aria-hidden="true">
                        <use xlink:href="#icon-GitHub"></use>
                    </svg>
                    https://github.com/sutaojie
                </li>
            </ul>
            <p class="online-resume">在线简历地址：###</p>
        </div>
        

         <section class="download">
        <p class="downloadResume-wrapper">
            <a class="downloadResume" href="./resume.pdf" download="前端工程师-苏赵勇-2018.pdf">下载简历</a>
        </p>
    </section>
        </div>
</template>

<script>
import '../assets/common/print.css'
export default{
    
}
</script>

<style>
section.download {
  position: fixed;
  top: 50%;
  transform: translateY(-50%);
  right: 0;
  z-index: 1;
}
section.download .downloadResume {
  display: inline-block;
  font-size: 14px;
  padding: 21px 22px;
  color: #f4f4f4;
  font-weight: bold;
  writing-mode: vertical-lr;
  transition: box-shadow 0.2s;
  letter-spacing: 1em;
  background: #1abc9c;
  font-family: Arial, sans-serif;
  border: solid 0 #e3edf4;
  border-bottom: 2px solid #3a9a95;
  -moz-border-radius: 4px;
  -webkit-border-radius: 4px;
  border-radius: 4px;
  opacity: 0.7;
}
section.download .downloadResume:hover {
  background: #2a8a85;
}

</style>
