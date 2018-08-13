<template>
<div class='display'>
    <div class="banner" :class="{'notPrint':isPrint}">
        <div class="mask "></div>
    </div>
    <main>
        <div  id="siteAbout" class="userCard" :class="{'notPrint':isPrint}"  v-if="personalInfo">
            <div class="pictureAndText clearfix">
                <div class="picture">
                    <img :src='personalInfo.photo' data-url="./img/resume.jpg" width=272 height=400 alt="头像">
                </div>
                <div class="text">
                  <span class="welcome">你好，我是一名前端工程师
                    <span class="triangle"></span>
                  </span>
                    <div >
                        <h1>{{personalInfo.name}}</h1>
                        <p>
                            {{personalInfo.brief}}
                        </p>
                    </div>
                    <hr>
                    <dl v-for="list in personalInfo.infoLists">
                        <dt>{{list.keyword}}</dt>
                        <dd>{{list.context}}</dd>
                    </dl>
                </div>
            </div>
            <footer class="media">
                <a   class="icon" v-for="media in personalInfo.medias" :href="media.link" target="_blank" :title="media.context">
                    <svg class="icon" aria-hidden="true">
                        <use :xlink:href="'#icon-'+media.icon"></use>
                    </svg>
                    
                </a>
               
            </footer>

        </div>
       
        <!--<p class="selfIntroduction">-->
        <!--</p>-->
    </main>
    </div>
</template>
<script src="https://at.alicdn.com/t/font_587178_vwi2iocx42c.js"></script>
<script>
import '../assets/common/common.css'
    export default{
         props: {
            iconName: {
                type: String,
                default: 'box'
            },
            width: {
                type: [Number, String],
                // default: 48
            },
            height: {
                type: [Number, String],
                // default: 48
            },
            iconColor: {
                type: String,
                default: 'currentColor'
            }
        },
        data(){
            return{
                isPrint:false,
                personalInfo:{
                    photo:'',
                    name:'苏赵勇',
                    brief:'男，24岁，大专，安徽财贸学院',
                    infoLists:[
                        {keyword:'所在城市' , context:'上海'},
                        {keyword:'手机号码' , context:'17682488600'},
                        {keyword:'微信号码' , context:'Coco-6120'},
                        {keyword:'网易邮箱' , context:'sutaojie@163.com'},
                        {keyword:'Gmail 邮箱' , context:'sutaojie@gmail.com'},
                    ],
                    medias:[
                        {link:'#' , context:'github', icon:'github'},
                        {link:'#' , context:'知乎', icon:'zhihu'},
                        {link:'#' , context:'eamil', icon:'email'},
                        
                    ]
                }
            }
        },
        created(){
            this.personalInfo.photo = require('../assets/img/resume.jpg')
        },
        beforeCreate(){
            
        }

    }
</script>

<style>
 .display{
    position: relative;
    
}
/*
main{
    position: absolute;
    top: 50%;
    left: 50%;
    transform: translate(-50%,0%);
} */
    .icon {
       width: 40px; height: 40px;
       vertical-align: -0.15em;
       fill: currentColor;
       overflow: hidden;
    }
.banner {
  height: 515px;
  /* background-image: url(img/rs-cover-2-2-1-1.jpg); */
  background-position: center center;
  background-size: cover;
}
.banner .mask {
  height: 515px;
  background-color: rgba(0, 0, 0, 0.8);
}
.userCard {
    position: absolute;
    /* left: 0; top: 0; right: 0; bottom: 0;
    margin: auto; */
    top: 50%;
    left: 50%;
    transform: translate(-50%,-50%);
    min-width: 940px;
    margin-top: 200px;
  margin-left: auto;
  margin-right: auto;
  background-color: #FFF;
  box-shadow: 0px 1px 5px 0px rgba(0, 0, 0, 0.5);
}
.userCard .welcome {
  background: #7E6EFC;
  color: #FFFFFF;
  display: inline-block;
  padding: 4px 16px;
  line-height: 22px;
  position: relative;
  margin-bottom: 10px;
}
.userCard .welcome .triangle {
  display: block;
  border: 10px solid transparent;
  widows: 0px;
  border-left-color: #7E6EFC;
  border-top-width: 0px;
  position: absolute;
  left: 4px;
  top: 100%;
}
.userCard .picture {
  float: left;
}
.userCard .picture img {
  background-attachment: cover;
}
.userCard .text {
  float: left;
  margin-left: 65px;
  width: 470px;
}
.userCard .text h1 {
  margin-top: 18px;
}
.userCard .text hr {
  margin: 20px 0;
}
.userCard .pictureAndText {
  padding: 50px;
}
.userCard dl dt,
.userCard dl dd {
  float: left;
  padding: 5px 0;
}
.userCard dl dt {
  width: 30%;
  font-weight: bold;
}
.userCard dl dd {
  width: 70%;
  color: #9da0a7;
}
.userCard > footer.media {
  background: #7E6EFC;
  text-align: center;
}
.userCard > footer.media > a {
  /* border: 1px solid black; */
  display: inline-block;
  width: 50px;

  padding: 5px 0;
  /*不写height加好办了*/
  line-height: 40px;
  border-radius: 50%;
  margin: 16px;
}
.userCard > footer.media > a:hover {
    /* width: 40px;
    height: 40px; */
    
  background: #CF5D5F;
}
.userCard svg {
  display: inline-block;
  vertical-align: baseline;
  margin-bottom: -2px; /* yes, I'm that particular about formatting */
}

</style>
