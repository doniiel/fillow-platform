<template>
    <div class="message-board-item">
      <div class="message_container">
      <div class="message">
        <ContentTitle class="message" fontSize="16px" color="#312A2A">{{ messageItem.userMessage }}</ContentTitle>
      </div>
      <ContentTitle class="timestamp" color="#737B8b" fontSize="10px">{{ messageItem.dateSent }}</ContentTitle>
    </div>
    <div class="user-info">
        <UserPortfolio :profileImage="profileImage" width="50" height="50" alt="User Image" class="user-img" />
      </div>
</div>
  </template>
  
  <script>
  import ContentTitle from './ContentTitle.vue';
  import UserPortfolio from './UserPortfolio.vue';
  export default {
    components:{
        ContentTitle,
        UserPortfolio,
    },
    props: {
      messageItem: {
        type: Object,
        required: true
      },
      profileImage: {
        type: String,
        required: true,
      },
    }
  };
  </script>
  
  <style scoped>

.message{
    background-color: #f3f0f9;
    padding: 10px;
    margin-bottom: 10px;
    border-radius:0.625rem 0.625rem 0;
    background-color: #f3f0f9;
    text-align: left;
}
.message-board-item{
    display: flex;
    align-items: center;
    margin: 21px 0px;
    width: 60%;
    float: right;
}

  </style>