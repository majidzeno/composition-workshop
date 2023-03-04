<template>
  <h2>Challenge 1</h2>
  <div class="wrapper">
    <h1 class="count">{{ countProp.count }}</h1>
    <div class="controllers">
      <button class="btn" @click="countProp.count--">-</button>
      <button class="btn" @click="countProp.count++">+</button>
    </div>
  </div>
</template>

<script>
import { reactive } from 'vue';
export default {
  setup() {
    const countProp = reactive({ count: 0 });
    return { countProp };
  },
};
</script>
 