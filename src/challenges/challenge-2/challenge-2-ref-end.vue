<!-- Exercise: Adding Reset Button -->
<!-- 1.✅ Extract the functionality that increase and decrease the count in separate methods increment and decrement -->
<!-- 2.✅ Add a "Reset" button that sets the count to 0 when clicked. -->
<!-- 3.✅ Define a resetCount method that sets the count to 0. -->
<!-- 4.✅ Bind the resetCount method to the "Reset" button's click event. -->

<template>
  <h2>Challenge 2</h2>
  <div class="wrapper">
    <h1 class="count">{{ count }}</h1>
    <div class="controllers">
      <button class="btn" @click="resetCount">Reset</button>
      <button class="btn" @click="decrement">-</button>
      <button class="btn" @click="increment">+</button>
    </div>
  </div>
</template>

<script>
import { ref } from 'vue';
export default {
  setup() {
    const count = ref(0);
    const increment = () => {
      count.value++;
    };

    const decrement = () => {
      count.value--;
    };

    const resetCount = () => {
      count.value = 0;
    };

    return { count, increment, decrement, resetCount };
  },
};
</script>
