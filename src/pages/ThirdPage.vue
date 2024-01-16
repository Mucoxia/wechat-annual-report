<template>
  <div class="column justify-center">
    <div class="a">
      这一年 各自说过最晚的一句话
      <br />
    </div>
    <div class="b slideInLeft animated">
      <span style="font-size: 5vw"> {{ user }}: </span>
      {{ content }}
    </div>
    <div class="d">
      {{ time }}
    </div>
    <div class="b slideInLeft animated">
      <span style="font-size: 5vw"> {{ user2 }}: </span>
      {{ content2 }}
    </div>
    <div class="d">
      {{ time2 }}
    </div>
    <div class="e" style="padding-top: 5vh; font-size: 5vw">那天在做什么还能记起来吗</div>
  </div>
</template>

<script>
import { latestMsg, latestMsg2 } from "../data.json";
export default {
  data() {
    return {
      ...latestMsg,
      ...latestMsg2
    };
  },
};
</script>

<style scoped>
.a {
  font-size: 5vw;
  animation-name: slide-top;
  animation-duration: 1s;
  animation-delay: 0.5s;
  animation-fill-mode: backwards;
}

.b {
  animation-delay: .5s;
  font-size: 5vw;
  font-weight: bolder;
  padding-top: 5vh;
  white-space: normal;
  text-overflow: ellipsis;
  overflow: hidden;
  line-height: 2;
  color: ebf45f;
}

.c {
  animation-name: slide-top;
  animation-duration: 1s;
  animation-delay: 1.5s;
  animation-fill-mode: backwards;
}

.d {
  font-size: 4vw;
  text-align: right;
  padding-top: 3vh;
  font-weight: bolder;
  animation-name: slide-top;
  animation-duration: 1s;
  animation-delay: 2s;
  animation-fill-mode: backwards;
}

.e {
  animation-name: slide-top;
  animation-duration: 1s;
  animation-delay: 2.5s;
  animation-fill-mode: backwards;
}
</style>