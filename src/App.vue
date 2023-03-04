<template>
  <div class="wrapper">
    <!-- <challenge-1-start /> -->
    <!-- <challenge-1-ref-end /> -->
    <!-- <challenge-1-reactive-end /> -->

    <!-- <challenge-2-start /> -->
    <!-- <challenge-2-ref-end /> -->
    <!-- <challenge-2-reactive-end /> -->

    <!-- <challenge-3-start /> -->
    <!-- <challenge-3-ref-end /> -->

    <!-- <challenge-4-start /> -->
    <!-- <challenge-4-ref-end /> -->

    <!-- <challenge-5-start /> -->
    <challenge-5-ref-end />

  </div>
</template>

<script>
// import Challenge1Start from './challenges/challenge-1/challenge-1-start.vue';
// import Challenge1RefEnd from './challenges/challenge-1/challenge-1-ref-end.vue';
// import Challenge1ReactiveEnd from './challenges/challenge-1/challenge-1-reactive-end.vue';

// import Challenge2Start from './challenges/challenge-2/challenge-2-start.vue';
// import Challenge2RefEnd from './challenges/challenge-2/challenge-2-ref-end.vue';
// import Challenge2ReactiveEnd from './challenges/challenge-2/challenge-2-reactive-end.vue';

// import Challenge3Start from './challenges/challenge-3/challenge-3-start.vue';
// import Challenge3RefEnd from './challenges/challenge-3/challenge-3-ref-end.vue';

// import Challenge4Start from './challenges/challenge-4/challenge-4-start.vue';
// import Challenge4RefEnd from './challenges/challenge-4/challenge-4-ref-end.vue';

// import Challenge5Start from './challenges/challenge-5/challenge-5-start.vue';
import Challenge5RefEnd from './challenges/challenge-5/challenge-5-ref-end.vue';

export default {
  components: {
    // Challenge1Start,
    // Challenge1RefEnd,
    // Challenge1ReactiveEnd
    
    // Challenge2Start,
    // Challenge2RefEnd,
    // Challenge2ReactiveEnd,

    // Challenge3Start,
    // Challenge3RefEnd,

    // Challenge4Start,
    // Challenge4RefEnd,

    // Challenge5Start,
    Challenge5RefEnd,
  },
};
</script>

<style lang="scss">
$dark-color: #3a1f60;
$light-color: #5b3687;
$highlight-color-1: #ee9a4f;
$highlight-color-2: #fabb62;

body {
  margin: 0;
  color: #fff;
  background: linear-gradient(-360deg, $light-color, darken($dark-color, 10%))
    no-repeat;
  min-height: 100vh;
  font-family: arial, sans-serif;
  display: flex;
  align-items: center;
  justify-content: center;
}

.wrapper {
  display: flex;
  align-items: center;
  justify-content: center;
  flex-flow: column;
}

.count {
  color: #fff;
  color: $highlight-color-1;
  font-size: 150px;
}

.controllers {
  display: flex;
  align-items: center;
  width: 35vw;
  justify-content: space-around;
}

.btn {
  cursor: pointer;
  color: #fff;
  display: flex;
  align-items: center;
  justify-content: center;
  // width: 150px;
  // height: 58px;
  font-size: 50px;
  padding: 18px 50px;
  font-size: 50px;
  border-radius: 10px;
  background: #3a1f60;
  box-shadow: inset 20px 20px 41px #1e1030, inset -20px -20px 41px #281642;
}

h2{
  position: absolute;
  left: 16px;
  top: 16px;
  color: #fff;
}
</style>