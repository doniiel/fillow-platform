<template>
    <div class="badge" :class="{ 'value': value > 0 }">
      <slot></slot>
      <div v-if="value > 0" class="notification-dot" :style="{ backgroundColor: color }">
        {{ value }}
      </div>
    </div>
  </template>
  
  <script>
  export default {
    props: {
      value: {
        type: Number,
        default: 0,
      },
      color: {
        type: String,
        default: 'red',
      },
    },
  };
  </script>
  
  <style scoped>
  .badge {
    position: relative;
    display: inline-block;
  }
  
  .notification-dot {
    position: absolute;
    top: -10px;
    right: -10px;
    width: 16px;
    height: 16px;
    border-radius: 50%;
    padding: 10px;
    color: white;
    display: flex;
    align-items: center;
    justify-content: center;
    font-size: 12px;
  }
  </style>