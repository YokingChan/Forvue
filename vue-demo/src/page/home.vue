<template>
  <div class="home-page">
    <v-header></v-header>
    <ul class="nav">
      <li v-for="item in navList">
        <img :src="item.address" />
        <span>{{ item.name }}</span>
      </li>
    </ul>
    <v-course :arrList="arrList"></v-course>
    <v-footer :footerList="footerList"></v-footer>
  </div>
</template>
<script>
import Header from "./../components/header";
import Course from "./../components/course";
import Footer from "./../components/footer";
import Web from "../assets/web.png";
import WebService from "../assets/webservice.png";
import Move from "../assets/move.png";
import Data from "../assets/data.png";
import BigData from "../assets/bigdata.png";
import course1 from "../assets/course1.jpg";
import course2 from "../assets/course2.jpg";
import course3 from "../assets/course3.jpg";
import course4 from "../assets/course4.jpg";
import course5 from "../assets/course5.jpg";
import home from "../assets/home.png";
import sea from "../assets/sea.png";
import download from "../assets/download.png";
import me from "../assets/me.png";
export default {
  components: {
    "v-header": Header,
    "v-course": Course,
    "v-footer": Footer
  },
  data() {
    return {
      navList: [
        { address: Web, name: "前端开发" },
        { address: WebService, name: "后端开发" },
        { address: Move, name: "移动开发" },
        { address: Data, name: "数据库" },
        { address: BigData, name: "大数据" }
      ],
      arrList: [
        { address: course1, title: "xxxx", msg: "前端开发" },
        { address: course2, title: "xxxx", msg: "后端开发" },
        { address: course3, title: "xxxx", msg: "移动开发" },
        { address: course4, title: "xxxx", msg: "数据库" },
        { address: course5, title: "xxxx", msg: "大数据" }
      ],
      footerList: [
        { address: home, name: "首页" },
        { address: sea, name: "发现" },
        { address: download, name: "下载" },
        { address: me, name: "我的" }
      ]
    };
  },
  mounted() {}
};
</script>
<style scoped>
.home-page .nav {
  height: 100px;
  padding-top: 65px;
  background: #f3f5f7;
  overflow-x: scroll;
  white-space: nowrap;
  font-size: 0;
}
.nav li {
  width: 88px;
  display: inline-block;
  text-align: center;
  font-size: 14px;
}
.nav li img {
  display: block;
  width: 32px;
  margin: 20px auto 12px;
}
</style>
