<template>
    <div class="search-container">
      <input type="text" class="search-input" placeholder="Search here..."/>
      <button class="search-button">
        <img src="@/assets/loupe.png" alt="">
      </button>
    </div>
  </template>
  
  <script>
  export default {
    name: "SearchBar",
  };
  </script>
  
  <style scoped>
  .search-container {
    display: flex;
    align-items: center;
    padding: 10px;
    width: 100%;
  }
  
  .search-input {
    flex: 1;
    padding: 15px;
    border: none;
    outline: none;
    transition: border-color 0.3s ease, box-shadow 0.3s ease;
    border-radius: 50px;
  }
  
  .search-input:hover {
    border-color: #e2e9e7;
    box-shadow: 0 0 10px rgba(0, 0, 0, 0.1);
  }
  
  .search-button {
    margin-left: -50px;
    border-radius: 50px;
    padding: 8px; 
    background-color: transparent;
    outline: none;
    cursor: pointer;
    transition: 0.5s;
    border: none;
  }
  .search-button img{
    height: 20px;
    width: 20px;
  }
  
  .search-button:hover {
   cursor: pointer;
  }
  
  </style>