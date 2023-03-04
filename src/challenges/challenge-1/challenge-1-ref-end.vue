<!-- Exercise using ref -->
<!-- ✅ Increase the count by using "ref" -->

<template>
  <h2>Challenge 1</h2>
  <div class="wrapper">
    <h1 class="count">{{ count }}</h1>
    <div class="controllers">
      <button class="btn" @click="count--">-</button>
      <button class="btn" @click="count++">+</button>
    </div>
  </div>
</template>

<script>
import { ref } from 'vue';

export default {
  setup() {
    const count = ref(0);
    return { count }
  },
};
</script>
