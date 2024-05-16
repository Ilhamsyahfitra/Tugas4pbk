<template>
    <div class="child1">
      <h2>Child Component 1</h2>
      <button @click="sendDataToParent">Send Data to Parent</button>
      <child-component2></child-component2>
    </div>
  </template>
  
  <script>
  import ChildComponent2 from './ChildComponent2.vue';
  
  export default {
    components: {
      ChildComponent2
    },
    methods: {
      sendDataToParent() {
        this.$emit('send-data', 'Data from Child 1');
      }
    }
  }
  </script>
  
  <style scoped>
  .child1 {
    margin: 10px;
    padding: 10px;
    border: 1px solid #000;
  }
  </style>
  