<template>
    <div>
      <h1>Home Page</h1>
      <p>Count: {{ count }}</p>
      <button @click="increment">Increment</button>
    </div>
  </template>
  
  <script>
  import { useMainStore } from '../store/index';
  import { computed } from 'vue'; // Add computed to handle reactivity
  
  export default {
    setup() {
      const store = useMainStore();
  
      // Use computed to make the count reactive
      const count = computed(() => store.count);
  
      return {
        count,
        increment: store.increment
      };
    }
  };
  </script>
  