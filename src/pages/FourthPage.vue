<template>
  <div class="column justify-center">
    <div class="a">
      <div class="text">
        这一年 我们发了{{ imgCount }}张图片，{{ memeCount }}个表情包。
      </div>
      <div class="text q-mt-xl">
        这一年 我们说过最多的词是
        <span class="value"> {{ content }} </span>
      </div>
      <span class="text">居然有</span>
      <span class="value"> {{ count }}次</span>
    </div>
    <div class="tips lightSpeedInRight animated">
      <div v-for="(tip, index) in tips" :key="index">
        {{ `${tip.content}: ${tip.count}次` }}
      </div>
    </div>
  </div>
</template>

<script>
import { mostWord, imgCount, memeCount } from "../data.json";
export default {
  data() {
    return {
      ...mostWord,
      imgCount,
      memeCount
    };
  },
};
</script>

<style scoped>
.tips {
  place-self: flex-end;
  animation-delay: .5s;
  margin-top: 10vh;
  float: right;
  font-size: 4vw;
  font-weight: bolder;
}

.value {
  font-weight: bolder;
  font-size: 7vw
}

.text {
  font-size: 5vw;
  font-weight: bolder;
}

.a {
  animation-name: slide-top;
  animation-duration: 1s;
  animation-delay: 0.5s;
  animation-fill-mode: backwards;
}

.b img {
  width: 100%;
  animation-name: slide-top;
  animation-duration: 1s;
  animation-delay: 1s;
  animation-fill-mode: backwards;
}
</style>