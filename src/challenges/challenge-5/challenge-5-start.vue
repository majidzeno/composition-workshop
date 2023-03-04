<!-- Exercise: Adding a "watch" property  -->
<!-- Add a watch property to the setup function in the component below. Use it to log a message to the console whenever the value of count changes. -->

<template>
  <h2>Challenge 5</h2>
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
