<template>
  <div class="column">
    <div class="title">
      <div class="a">2023</div>
      <div class="b">
        WECHAT
        <br />
        REPORT
      </div>
      <div class="c">年度聊天报告</div>
    </div>
    <div class="human">
      <div class="boy">
        <q-img class="a" src="../assets/images/boy.png" />
        <q-img class="b" src="../assets/images/cloud1.png" />
      </div>
      <div class="girl">
        <q-img class="a" src="../assets/images/girl.png" />
        <q-img class="b" src="../assets/images/cloud2.png" />
      </div>
    </div>
  </div>
</template>

<script>
export default {};
</script>

<style scoped>
.human {
  position: absolute;
  top: 15vh
}

.title {
  color: white;
  line-height: 1;
  display: grid;
  grid-template-columns: max-content 1fr;
}

.title .a {
  font-size: 20vw;
}

.title .b {
  padding-top: 1em;
  font-size: 5vw;
  margin-left: 5vw;
}

.title .c {
  font-size: 7vw;
}

.human .boy {
  position: relative;
  top: -10vh;
  animation: up-down 2s ease-in-out infinite both;
}

.human .girl {
  width: 40%;
  position: relative;
  top: -15vh;
  left: 40vw;
  animation: up-down 2s ease-in-out infinite both;
}

@keyframes up-down {
  0% {
    transform: translateY(1vh);
  }

  50% {
    transform: translateY(0vh);
  }

  100% {
    transform: translateY(1vh);
  }
}

.human .boy .a {
  width: 27vw;
  position: relative;
  left: 10vw;
  top: 15vh;
  z-index: 2;
}

.human .boy .b {
  width: 50vw;
  position: relative;
  left: -30vw;
  top: 20vh;
}

.human .girl .a {
  width: 50vw;
  position: relative;
  left: 5vw;
  top: 15vh;
  z-index: 2;
}

.human .girl .b {
  width: 50vw;
  position: relative;
  left: 5vw;
  top: -5vh;
}

.star {
  position: absolute;
  bottom: 10vh;
  left: calc(50vw - 15vw);
}

.star .circle {
  width: 30vw;
  height: 30vw;
  border-radius: 100%;
  text-align: center;
  color: white;
  animation: hvr-ripple-out 2s ease-in-out infinite alternate both;
}

@keyframes hvr-ripple-out {
  100% {
    transform: scale(1.1);
  }
}

.star .label {
  position: absolute;
  font-size: 4vw;
  text-align: center;
  font-weight: lighter;
  top: 14vw;
  left: 9vw;
  color: #F9F7C9;
  font-weight: bold;
}
</style>