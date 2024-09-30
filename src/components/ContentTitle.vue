<template>
    <h1 :style="titleStyles">
      <slot></slot>
    </h1>
  </template>
  
  <script>
  export default {
    props: {
      color: {
        type: String,
        default: 'black',
      },
      fontSize: {
        type: String,
        default: '24px',
      },
      fontWeight: {
        type: String,
        default: 'normal',
      },
    },
    computed: {
      titleStyles() {
        return {
          color: this.color,
          fontSize: this.fontSize,
          fontWeight: this.fontWeight,
        };
      },
    },
  };
  </script>
  
  <style scoped>
  *{
    display: flex;
    align-items: center;
    gap: 10px;
  }
  </style>