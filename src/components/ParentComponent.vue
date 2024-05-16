<template>
    <div class="parent">
      <h1>Parent Component</h1>
      <child-component1 @send-data="displayData"></child-component1>
      <slot-component>
        <template v-slot:header>
          <h2>This is a header from Parent</h2>
        </template>
        <template v-slot:content>
          <p>This is some content from Parent</p>
        </template>
      </slot-component>
      <p>{{ message }}</p>
    </div>
  </template>
  
  <script>
  import ChildComponent1 from './ChildComponent1.vue';
  import SlotComponent from './SlotComponent.vue';
  
  export default {
    components: {
      ChildComponent1,
      SlotComponent
    },
    data() {
      return {
        message: ''
      }
    },
    methods: {
      displayData(data) {
        this.message = data;
      }
    }
  }
  </script>
  
  <style scoped>
  .parent {
    padding: 20px;
    border: 2px solid #ccc;
  }
  </style>
  