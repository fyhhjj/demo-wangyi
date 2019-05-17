<template>
  <div class="home">
    <div class="header">
      <div class="left_sidebar"></div>
      <ul class="top_warp">
        <li
          v-for="(item, index) in toptext"
          :key="index"
          :class="{active:isActive==index}"
          @click="isActive=index"
        >{{item.text}}</li>
      </ul>
      <div class="search"></div>
    </div>
    <main>
      <mPage :is-active="isActive"></mPage>
    </main>
  </div>
</template>

<script>
// @ is an alias to /src
import mPage from "../components/mainPage";

export default {
  name: "home",
  data() {
    return {
      toptext: [
        { text: "我的" },
        { text: "发现" },
        { text: "朋友" },
        { text: "视频" }
      ],
      isActive: 0
    };
  },
  components: {
    mPage
  }
};
</script>
<style lang="less" scoped>
.header {
  margin: 10px 0;
  display: flex;
  justify-content: flex-start;
  div {
    width: 100px;
    height: 100px;
  }
  .top_warp {
    display: flex;
    justify-content: flex-start;
    width: 73.5vw;
    li {
      font-size: 30px;
      width: 25%;
      line-height: 100px;
    }
  }
}
.active {
  font-size: 35px !important;
  color: #333;
  font-weight: 500;
}
</style>

