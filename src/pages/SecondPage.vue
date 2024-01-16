<template>
  <div class="column justify-center">
    <div class="a animated flipInX">我们又在一起了一年</div>
    <div class="b">年年有我，岁岁有我</div>
    <div class="c">出发去看看我们的2023吧~</div>
  </div>
</template>

<script>
export default {};
</script>

<style scoped>
.a,
.b,
.c {
  text-align: center;
  color: white;
}

.a {
  font-size: 8vw;
  animation-delay: .5s;
}

.b {
  font-size: 6vw;
  padding-top: 5vh;
  animation-name: slide-top;
  animation-duration: 1s;
  animation-delay: 1s;
  animation-fill-mode: backwards;
}

.c {
  font-size: 5vw;
  font-weight: lighter;
  animation-name: slide-top;
  animation-duration: 1s;
  animation-delay: 1.5s;
  animation-fill-mode: backwards;
}
</style>