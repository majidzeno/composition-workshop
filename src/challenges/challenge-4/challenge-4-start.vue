<!-- Exercise: Adding lifecycle hooks  -->
<!-- 🚨 Disclaimer: Please note that this exercise only covers a few of the available lifecycle hooks
in the Composition API. We will focus on practicing the usage of the onMounted, onBeforeUpdate,
and onUpdated hooks. Keep in mind that there are more lifecycle hooks available for different use cases,
and this exercise should not be considered an exhaustive overview of all available hooks. -->

<!-- Add a lifecycle hook to the component that logs a message to the console before the component is mounted. -->
<!-- Add a lifecycle hook to the component that logs a message to the console when the component is mounted. -->
<!-- Add a lifecycle hook to the component that logs a message to the console when the component is updated. -->

<template>
  <h2>Challenge 4</h2>
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
