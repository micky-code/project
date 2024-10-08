<template>
    <div>
      <h2>{{ msg }}</h2>
      <button @click="sendDataToParent">Send Data to Parent</button>
    </div>
  </template>
  
  <script>
  export default {
    props: ['msg'],
    methods: {
      sendDataToParent() {
        this.$emit('childEvent', 'Hello Parent, from Child!');
      }
    }
  };
  </script>
  