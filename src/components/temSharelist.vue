<!-- 文章列表 -->
<template>
  <el-row class="sharelistBox">
    <div class="prompt">
      <i class="fa fa-volume-up fa-fw"></i>&nbsp;&nbsp;欢迎来到我的博客~>ω
    </div>
    <el-col class="s-item tcommonBox el-col el-col-24" v-for="(item) in items" :key="item.index">
      <header>
        <h1>
          <a @click="$router.push(item.push)">{{item.title}}</a>
        </h1>
        <div class="ui label">小项目</div>
      </header>
      <div class="article-content">
        <p style="text-indent:2em;">{{item.description}}</p>
        <p style="max-height:300px;overflow:hidden;text-align:center;">
          <img :src="item.image" class="maxW" />
        </p>
      </div>
      <div class="viewdetail">
        <a @click="$router.push(item.push)" class="tcolors-bg">阅读全文</a>
      </div>
    </el-col>
  </el-row>
</template>
 
<script>
export default {
  name: "Share",
  data() {
    return {
      items: [
        {
          title: "打字游戏和弹球小游戏",
          description: "放松必备小游戏:",
          image: "/img/demo/Pinball.png",
          push: "/game",
        },
        {
          title: "记账本和卡片的使用",
          description: "手写记账本和卡片你值得拥有:",
          image: "/img/demo/记账本.png",
          push: "/Note",
        },
        {
          title: "语音识别和语音合成",
          description: "HTML5语音合成Speech Synthesis API:",
          image: "/img/demo/speeh.png",
          push: "/Speech",
        },
        {
          title: "web-API接口的应用",
          description: "使用API接口获取想要的东西并展示再web页面上:",
          image: "/img/demo/caidan.png",
          push:"/Api",
        },
        {
          title: "很火的电影院选座",
          description: "电影价格和影片的关系，选座的实现:",
          image: "/img/demo/movies.png",
          push:"/movie"
        },
        {
          title: "web页面播放、音频",
          description: "web页面视频和音频播放器的构成:",
          image: "/img/demo/musicplay.png",
          push:"/play"
        },
        {
          title: "计时和新年倒计时",
          description: "利用web的日期时间实现秒表和新年倒计时:",
          image: "/img/demo/newyear.png",
          push:"./countdown"
        },
        {
          title: "js入门之注册页面的实现",
          description: "常见注册页面的实现：",
          image: "/img/demo/zhuce1.png",
          push:"./register"
        },
        {
          title: "初学html+css",
          description: "一个小白自学HTML和css:",
          image: "/img/demo/css.png",
          push:"css"
        },
      ],
    };
  },
};
</script>

<style>
/*分享标题*/
.prompt {
  margin-top: 40px;
  width: auto;
  border: 1px #999 dashed;
  border-radius: 5px;
  color: #999;
  padding: 20px 5px;
  text-align: center;
  font-size: 20px;
}
.shareTitle {
  margin-bottom: 40px;
  position: relative;
  border-radius: 5px;
  background: #fff;
  padding: 15px;
}
.shareclassTwo {
  width: 100%;
}
.shareclassTwo li {
  display: inline-block;
}
.shareclassTwo li a {
  display: inline-block;
  padding: 3px 7px;
  margin: 5px 10px;
  color: #fff;
  border-radius: 4px;
  background: #64609e;
  border: 1px solid #64609e;
  transition: transform 0.2s linear;
  -webkit-transition: transform 0.2s linear;
}
.shareclassTwo li a:hover {
  transform: translate(0, -3px);
  -webkit-transform: translate(0, -3px);
}
.shareclassTwo li a.active {
  background: #fff;
  color: #64609e;
}
/*文章列表*/
.sharelistBox {
  transition: all 0.5s ease-out;
  font-size: 15px;
}
.prompt {
  margin-top: 40px;
  width: auto;
  border: 1px #999 dashed;
  border-radius: 5px;
  color: #999;
  padding: 20px 5px;
  text-align: center;
  font-size: 20px;
  background: rgba(255, 255, 255, 0.8);
}
a {
  cursor: pointer;
  color:red;
}
</style>
