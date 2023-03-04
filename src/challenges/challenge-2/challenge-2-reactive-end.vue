<!-- Exercise: Adding Reset Button -->
<!-- 1.✅ Extract the functionality that increase and decrease the count in separate methods increment and decrement -->
<!-- 2.✅ Add a "Reset" button that sets the count to 0 when clicked. -->
<!-- 3.✅ Define a resetCount method that sets the count to 0. -->
<!-- 4.✅ Bind the resetCount method to the "Reset" button's click event. -->

<template>
  <h2>Challenge 2</h2>
  <div class="wrapper">
    <h1 class="count">{{ state.count }}</h1>
    <div class="controllers">
      <button class="btn" @click="resetCount">Reset</button>
      <button class="btn" @click="decrement">-</button>
      <button class="btn" @click="increment">+</button>
    </div>
  </div>
</template>

<script>
import { reactive } from 'vue';
export default {
  setup() {
    const state = reactive({ count: 0 });
    const increment = () => {
      state.count++;
    };

    const decrement = () => {
      state.count--;
    };

    const resetCount = () => {
      state.count = 0;
    };

    return { state, increment, decrement, resetCount };
  },
};
</script>
