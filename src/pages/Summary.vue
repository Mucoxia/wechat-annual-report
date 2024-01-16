<template>
  <div class="v">
    <div class="a">
      <div class="b">#2023</div>
      <div class="c">年度聊天报告</div>
      <div class="d">关键词</div>
      <div class="e">哈哈哈：76次</div>
      <div class="f"></div>
      <div class="d">爱意词</div>
      <div class="e">晚安：47次</div>
      <div class="f"></div>
      <div class="d">话痨月</div>
      <div class="e" style="font-size: 5vw">9月：2065条</div>
      <div class="f"></div>
      <div class="h">
        <img class="p" src="../assets/images/people.webp" />
        <img class="y" src="../assets/images/cloud2.png" />
      </div>
      <div class="j">再见</div>
      <div class="i">2023</div>
    </div>
  </div>
</template>

<script>
export default {
  data() {
    return {
    };
  },
};
</script>

<style scoped>
.v {
  background-image: linear-gradient(#80BCBD, #F9F7C9);
  height: 100%;
  color: #80BCBD;
}

.a {
  border-radius: 10px;
  margin-top: 10vh;
  height: 70vh;
  border: 5px #AAD9BB solid;
  background: #fef9f9;
  padding: 5vw;
}

.b {
  font-size: 13vw;
  padding-bottom: unset;
}

.c {
  font-size: 5vw;
  font-weight: 700;
  padding-bottom: 5vh;
}

.d {
  color: 80BCBD;
  font-weight: bold;
  font-size: 5vw;
}

.e {
  margin-top: 1vh;
  color: F9F7C9;
  font-weight: bold;
  font-size: 5vw;
}

.f {
  height: 6px;
  background: #AAD9BB;
  width: 30vw;
  margin-bottom: 2vh;
}

.p {
  position: absolute;
  width: 53vw;
  left: 46vw;
  top: 33vh;
  z-index: 2;
}

.y {
  position: absolute;
  width: 60vw;
  left: 36vw;
  top: 50vh;
}

.i,
.j {
  position: absolute;
  color: #80BCBD;
}

.j {
  font-size: 10vw;
  top: 25vh;
  left: 55vw;
}

.i {
  font-size: 10vw;
  top: 32vh;
  left: 60vw;
}
</style>