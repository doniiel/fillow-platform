<template>
    <div class="icons">
      <div class="img" :style="{ color: color, fontSize: size, backgroundColor:backgroundColor}">
        <i v-if="iconType === 'star'" class="fas fa-star"></i>
        <i v-if="iconType === 'bell'" class="fas fa-bell"></i>
        <i v-if="iconType === 'message'" class="fas fa-envelope"></i>
        <i v-if="iconType === 'date'" class="fas fa-calendar-alt"></i>
        <i v-if="iconType === 'plus'" class="fa-solid fa-plus"></i>
        <i v-if="iconType === 'dots'" class="fa-solid fa-ellipsis-vertical"></i>
        <i v-if="iconType === 'f'" class="fa-solid fa-f"></i>
        <i v-if="iconType === 'video'" class="fa-solid fa-video"></i>
        <i v-if="iconType === 'search'" class="fa-solid fa-magnifying-glass"></i>
        <i v-if="iconType === 'left'" class="fa-solid fa-arrow-left"></i>
        <i v-if="iconType === 'right'" class="fa-solid fa-arrow-right"></i>
        <i v-if="iconType === 't'" class="fa-solid fa-t"></i>
        <i v-if="iconType === 'i'" class="fa-solid fa-i"></i>
        <i v-if="iconType === 'b'" class="fa-solid fa-b"></i>
        <i v-if="iconType === 'smile'" class="fa-solid fa-face-smile"></i>
        <i v-if="iconType === 'paperclip'" class="fa-solid fa-paperclip"></i>
        <i v-if="iconType === 'plane'" class="fa-solid fa-paper-plane"></i>
        <i v-if="iconType === 'info'" class="fa-solid fa-circle-info"></i>
        <i v-if="iconType === 'chart'" class="fa-solid fa-chart-line"></i>
        <i v-if="iconType === 'bootstrap'" class="fa-solid fa-bootstrap"></i>
        <i v-if="iconType === 'heart'" class="fa-solid fa-heart"></i>
        <i v-if="iconType === 'user'" class="fa-solid fa-user"></i>
        <i v-if="iconType === 'file'" class="fa-solid fa-file"></i>
        <i v-if="iconType === 'table'" class="fa-solid fa-table"></i>
        <i v-if="iconType === 'clone'" class="fa-solid fa-clone"></i>
        <i v-if="iconType === 'phone'" class="fa-solid fa-phone"></i>
        <i v-if="iconType === 'storm'" class="fa-solid fa-bolt"></i>
        <i v-if="iconType === 'dot'" class="fa-solid fa-ellipsis"></i>
        
      </div>
    </div>
  </template>
  
  <script>
  export default {
    props: {
      size: {
        type: String,
        default: "20px",
      },
      color: {
        type: String,
        default: "gray",
      },
      backgroundColor:{
        type: String,
      },
      iconType: String,
    },
  };
  </script>
  <style scoped>
</style>