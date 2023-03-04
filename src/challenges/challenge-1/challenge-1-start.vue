<!-- Exercise using ref -->
<!-- Increase the count by using "ref" -->
<!-- 🎁 Bonus: Let's replace the "ref" by "reactive" -->

<template>
  <h2>Challenge 1</h2>
  <div class="wrapper">
    <h1 class="count">{{ count }}</h1>
    <div class="controllers">
      <button class="btn">-</button>
      <button class="btn">+</button>
    </div>
  </div>
</template>

<script>
export default {
  data() {
    return {
      count: 0,
    };
  },
};
</script>
