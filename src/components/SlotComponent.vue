<template>
    <div class="slot">
      <slot name="header"></slot>
      <slot name="content"></slot>
    </div>
  </template>
  
  <script>
  export default {
  }
  </script>
  
  <style scoped>
  .slot {
    margin: 10px;
    padding: 10px;
    border: 1px dashed #000;
  }
  </style>
  