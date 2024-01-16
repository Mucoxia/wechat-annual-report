<template>
  <q-carousel v-model="slide" vertical transition-prev="slide-down" transition-next="slide-up" swipeable animated
    control-color="white" padding class="background text-white shadow-1 rounded-borders">
    <q-carousel-slide :name="index" class="column no-wrap" v-for="(component, index) in components" :key="index">
      <component :is="component" class="slide-page" :class="'page' + index"></component>
      <div v-if="slide !== 8" class="footer"></div>
    </q-carousel-slide>
  </q-carousel>
</template>

<script>
import FirstPage from "./FirstPage";
import SecondPage from "./SecondPage";
import ThirdPage from "./ThirdPage";
import FourthPage from "./FourthPage";
import FifthPage from "./FifthPage";
import SixthPage from "./SixthPage";
import SummaryPage from './Summary'

import ApexCharts from 'apexcharts'
window.ApexCharts = ApexCharts
export default {
  name: 'PageIndex',
  components: {
    FirstPage,
    SecondPage,
    ThirdPage,
    FourthPage,
    FifthPage,
    SixthPage,
    SummaryPage
    // SeventhPage,
    // EighthPage,
    // NinthPage,
  },
  data() {
    return {
      components: [
        FirstPage,
        SecondPage,
        ThirdPage,
        FourthPage,
        FifthPage,
        SixthPage,
        SummaryPage
        // SeventhPage,
        // EighthPage,
        // NinthPage,
      ],
      slide: 0,
    }
  }
}
</script>
<style lang="scss" scoped>
.slide-page {
  height: 75vh
}

.background {
  height: 100vh;
  background-image: linear-gradient($color1, $color4);
}

.footer {
  background-image: url("../assets/images/foot.png");
  background-size: cover;
  width: 100%;
  height: 25vh;
  position: absolute;
  bottom: 0vh;
  overflow: hidden;
}
</style>