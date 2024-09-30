<template>
    <div class="drawer" :class="{'open': open}">
       <button class="toggle-drawer" @click="toggleDrawer">
         <span v-if="open">&times;</span>
         <span v-else>&#9776;</span>
       </button>
       <div class="drawer-content">
         <slot></slot>
       </div>
    </div>
   </template>
   
   <script>
   export default {
    data() {
       return {
         open: false,
       };
    },
    methods: {
       toggleDrawer() {
         this.open = !this.open;
       },
       openDrawer() {
         this.open = true;
       },
       closeDrawer() {
         this.open = false;
       },
    },
   };
   </script>
   
   <style scoped>
   .drawer {
    position: fixed;
    top: 0;
    left: 0;
    width: 250px;
    height: 100%;
    background-color: #fff;
    box-shadow: 0 2px 5px rgba(0, 0, 0, 0.3);
    overflow-x: hidden;
    transition: all 0.3s ease;
   }
   
   .drawer .toggle-drawer {
    position: absolute;
    top: 20px;
    right: -40px;
    font-size: 24px;
    color: #000;
    background-color: transparent;
    border: none;
    cursor: pointer;
    transition: all 0.3s ease;
   }
   
   .drawer .toggle-drawer:hover {
    color: #777;
   }
   
   .drawer-content {
    padding: 20px;
   }
   
   .drawer.open {
    transform: translateX(0);
   }
   
   .drawer:not(.open) {
    transform: translateX(-100%);
   }
   </style>