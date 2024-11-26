<template>
    <div>
      <child-component @data-from-child="handleData"></child-component>
      <p>Data from child: {{ childData }}</p>
    </div>
  </template>
  
  <script>
  import ChildComponent from './ChildComponent.vue';
  
  
  export default {
    components: {
      ChildComponent
    },
    data() {
      return {
        childData: ''
      };
    },
    methods: {
      handleData(data) {
        // Handle data sent from the child
        this.childData = data;
      }
    }
  };
  </script>
  