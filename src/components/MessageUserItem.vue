<template>
    <div class="message_main" :class="{ 'single-item': imgSrc.length === 1 }">
      <div class="ContentUser">
        <UserPortfolio
          v-for="(item, index) in imgSrc"
          :key="index"
          :profileImage="item.userImages"
          :width="width"
          :height="height"
        ></UserPortfolio>
      </div>
  
      <div class="message_content">
        <div class="ContentTitle">
          <ContentTitle color="#312A2A" fontSize="14px" fontWeight="800">{{ contentTitle }}</ContentTitle>
          <ContentTitle color="#9DA1A5" fontSize="12px">{{ contentTime }}</ContentTitle>
        </div>
        <div class="ContentDescription">
          <ContentTitle color="#9DA1A5" fontSize="14px">{{ contentDescription }}</ContentTitle>
        </div>
      </div>
    </div>
  </template>

<script>
import UserPortfolio from './UserPortfolio.vue';
import ContentTitle from './ContentTitle.vue';

export default {
  components: {
    UserPortfolio,
    ContentTitle,
  },
  props: {
   imgSrc: {
      type: Array,
    default: () => [],
  },
    contentTitle: {
      type: String,
      default: '',
    },
    contentDescription: {
      type: String,
      default: '',
    },
    contentTime: {
      type: String,
      default: '',
    },
    width: {
      type: Number,
      default: 100, 
    },
    height: {
      type: Number,
      default: 100, 
    },
  },
  data() {
    return {};
  },
};
</script>
  
  <style scoped>
  .message_main {
    display: flex;
    align-items: center;
    padding: 12px 20px;
    justify-content: space-around;
    border-bottom: 1px solid #d6dadd;
  }
  
  .ContentTitle {
    display: flex;
    justify-content: space-between;
    margin-bottom: 15px;
  }
  
  .ContentUser {
    display: grid;
    grid-template-columns: repeat(2, 1fr);
    gap: 10px;
  }
  
  .single-item .ContentUser {
    grid-template-columns: repeat(1, 1fr);
  }
  </style>