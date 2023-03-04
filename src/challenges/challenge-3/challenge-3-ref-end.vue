<!-- Exercise: Adding a computed property  -->
<!-- ✅ 1. Add a computed property isPositive to the setup() function. -->
<!-- ✅ 2. isPositive should return true if state.count is greater than or equal to 0, and false otherwise. -->
<!-- ✅ 3. In the template, display the value of isPositive in h2 element below the count display. -->
<!-- ✅ 4. Show a message that says "The count is positive" if isPositive is true, and "The count is negative" if isPositive is false., P.S: make the "message" a computed property too -->

<template>
  <h2>Challenge 3</h2>
  <div class="wrapper">
    <h3>{{ message }}</h3>
    <h1 class="count">{{ count }}</h1>

    <div class="controllers">
      <button class="btn" @click="resetCount">Reset</button>
      <button class="btn" @click="decrement">-</button>
      <button class="btn" @click="increment">+</button>
    </div>
  </div>
</template>

<script>
import { ref, computed } from 'vue';
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

    const isPositive = computed(() => {
      return count.value >= 0;
    });

    const message  = computed(()=>{
      return isPositive.value ? "The count is positive" : "The count is negative"
    })

    return { count, increment, decrement, resetCount, isPositive, message };
  },
};
</script>
