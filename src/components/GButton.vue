<template>
    <div class="btn-group">
      <button
        v-for="item in items"
        :key="item.status"
        class="btn btn-xs"
        :class="{ 'active': val === item.status }"
        @click="$emit('change-status', item.status)"
      >
        {{ item.title }}
      </button>
    </div>
  </template>
  
  <script>
  export default {
    props: {
      val: Number,
      items: {
        type: Array,
        default: () => [],
      },
    },
  };
  </script>
  
  <style scoped>
  .btn-group{
    padding: 3px;
    background-color: #886cc01a;
    border-radius: 10px;

  }
  .btn {
    flex: 1;
    background-color: transparent; 
    border: none;
    border-radius: 6px;
    color: #737b8b; 
    padding: 8px 16px;
    cursor: pointer;
    transition: background-color 0.3s, color 0.3s, box-shadow 0.3s;
    
  }
  
  .btn:hover {
    background-color: #aba4ad; 
  }
  
  .active {
    background-color: #886cc0;
    color: #ffffff; 
  }
  
  .btn-group {
    display: flex;
  }
  </style>