<template>
    <footer class="footer">
      <div class="container">
        <ContentTitle color="#9fa4a6" fontSize="13px">Fillow Saas Admin © 2023 All Rights Reserved</ContentTitle>
        <ContentTitle color="#9fa4a6" fontSize="13px">Made with <PageIcons iconType="heart"></PageIcons> by DexignLab</ContentTitle>
      </div>
    </footer>
  </template>
  
  <script>
  import ContentTitle from './ContentTitle.vue';
  import PageIcons from './PageIcons.vue'
  export default {
    components:{
        ContentTitle,
        PageIcons,
    }
  };
  </script>
  
  <style scoped>
  .footer {
    background-color: #ffffff;
    color: #9fa4a6;
    padding: 20px 0;
    text-align: center;
  }
  
  .container {
    font-size: 13px;
    max-width: 1200px;
    margin: 0 auto;
    padding: 20px;
  }
  .container h1{
    margin-bottom: 15px;
    line-height: 25px;
  }
  .container b{
    color: #886CC0;
  }
  </style>
  