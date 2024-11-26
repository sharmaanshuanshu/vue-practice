<template>
    <button @click="sendData">Send Data to Parent</button>
  </template>
  
  <script>
  export default {
    methods: {
      sendData() {
        // Emit the data to the parent
        this.$emit('data-from-child', 'Hello Parent!');
      }
    }
  };
  </script>
  