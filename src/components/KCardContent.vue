<template>
    <div v-for="(card, index) in cards" :key="index" class="content_card">
      <div class="card_headres">
        <ContentTitle  :color="card.titleColor" fontSize="14px" fontWeight="400">
          {{ card.title }}
        </ContentTitle>
        <PageIcons iconType="dot"></PageIcons>
      </div>
      <div class="description">
        <ContentTitle color="#312a2a" fontSize="18px" fontWeight="700">
        {{ card.description }}
      </ContentTitle>
      </div>

      <ConProgressbar  :percentage="card.percentage" :progressBarColor="card.progressBarColor"></ConProgressbar>
      <div class="card_footer">
        <UserPortfolio width="40" height="40" :profileImage="card.userSrc"></UserPortfolio>
        <div class="mg">
          <UserPortfolio width="40" height="40" :profileImage="card.userSrc"></UserPortfolio>
        </div>
        <div class="mg">
          <UserPortfolio width="40" height="40" :profileImage="card.userSrc"></UserPortfolio>
        </div>
        <ContentTitle color="#9da1a5" fontSize="14px">{{ card.date }}</ContentTitle>
      </div>
    </div>
  </template>
  
  <script>
  import UserPortfolio from './UserPortfolio.vue';
  import PageIcons from './PageIcons.vue';
  import ContentTitle from './ContentTitle.vue';
  import ConProgressbar from './ConProgressbar.vue';
  
  export default {
    components: {
      ContentTitle,
      PageIcons,
      ConProgressbar,
      UserPortfolio,
    },
    props: {
      cards: {
        type: Array,
        required: true,
        default: () => [],
      },
    },
  };
  </script>
  
  <style scoped>
  .content_card {
    background-color: #ffffff;
    padding: 20px;
    border-radius: 10px;
    margin-bottom: 15px;
  }
  
  .card_headres {
    display: flex;
    align-items: center;
    justify-content: space-between;
  }
  
  .card_footer {
    display: flex;
    align-items: center;
    justify-content: space-between;
  }
  .description{
    text-align: left;
    margin-bottom: 20px;
    width: 80%;
  }
  .mg{
    margin-left: -50px;
  }
  </style>