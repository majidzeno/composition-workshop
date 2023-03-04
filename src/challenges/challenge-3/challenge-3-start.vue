<!-- Exercise: Adding a computed property  -->
<!-- 1. Add a computed property isPositive to the setup() function. -->
<!-- 2. isPositive should return true if state.count is greater than or equal to 0, and false otherwise. -->
<!-- 3. In the template, display the value of isPositive in a paragraph element below the count display. -->
<!-- 4. Use the v-if directive to conditionally render a message that says "The count is positive" if isPositive is true, and "The count is negative" if isPositive is false. -->

<template>
  <h2>Challenge 3</h2>
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
