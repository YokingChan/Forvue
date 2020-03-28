<template>
  <div class="detail-page">
    <div class="video">
      <video
        src="https://cn-jxnc-cmcc-bcache-02.bilivideo.com/upgcxcode/91/81/163788191/163788191-1-16.mp4?e=ig8euxZM2rNcNbdlhoNvNC8BqJIzNbfq9rVEuxTEnE8L5F6VnEsSTx0vkX8fqJeYTj_lta53NCM=&uipk=5&nbs=1&deadline=1585415484&gen=playurl&os=bcache&oi=3746231042&trid=7fd2d5fd69ee4426b34d34a9cc693f69h&platform=html5&upsig=67043972b6781259bd7181dedf0547eb&uparams=e,uipk,nbs,deadline,gen,os,oi,trid,platform&mid=0&origin_cdn=ks3"
        controls="controls"
      ></video>
      <router-link to="/"><div class="video-back"><</div></router-link>
    </div>
    <ul class="nav">
      <li v-for="item in arr">{{ item }}</li>
    </ul>
    <div class="title">
      <h1>{{ title }}</h1>
      <p>{{ des }}</p>
    </div>
    <div class="question">
      <li v-for="(item, index) in arrQuestion">
        <h1>{{ arrTitle[index] }}</h1>
        <p v-html="item"></p>
      </li>
    </div>
  </div>
</template>
<script>
export default {
  data() {
    return {
      arr: [],
      title: "",
      des: "",
      arrQuestion: [],
      arrTitle: ["课程须知", "老师告诉你能学到什么？"]
    };
  },
  mounted() {
    this.arr = ["动漫", "详情", "评论", "问答", "攻略"];

    this.title = "动漫燃-大佬们的最终之战！";
    this.des = "各界大佬的集合出战";

    this.arrQuestion = [
      "本课程适合宅男，研发人员以及对动漫感兴趣的人群",
      `
			(1)动漫展相关的所有API<br/> 
			(2)解锁动漫实现各种属性技能<br/> 
			(3)观看最酷炫的动漫特效<br/>
			(4)了解动漫热血剧情！`
    ];
  }
};
</script>
<style scoped>
.video {
  position: relative;
  height: 191px;
}
.video video {
  width: 100%;
  height: 100%;
}
.video-back {
  position: absolute;
  top: 21px;
  left: 16px;
  text-align: center;
  color: #fff;
  font-size: 18px;
  line-height: 32px;
  border-radius: 3px;
  width: 32px;
  height: 32px;
  background: rgba(0, 0, 0, 0.5);
}

.nav {
  position: relative;
  z-index: 1;
  display: flex;
  box-shadow: 0 2px 4px 0 rgba(0, 0, 0, 0.1);
}
.nav li {
  flex: 1;
  text-align: center;
  height: 44px;
  line-height: 44px;
  background: #fff;
  font-size: 14px;
}
.title {
  padding: 24px 0 0 20px;
  margin-bottom: 8px;
box-shadow: 0 2px 4px 0 rgba(0, 0, 0, 0.1);
}
.title h1 {
  font-size: 16px;
  color: #2b333b;
}
.title p {
  font-size: 14px;
  color: #71777d;
  padding: 16px 0 34px;
  width: 335px;
}
.question {
  padding: 20px;
  background: #fff;
}
.question li h1 {
  font-size: 14px;
  color: #2b333b;
}
.question li p {
  padding: 12px 0 0 30px;
  font-size: 14px;
  color: #71777d;
}
.question li:nth-child(1) {
  padding-bottom: 24px;
}
</style>
