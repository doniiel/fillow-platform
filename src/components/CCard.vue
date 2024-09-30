<template>
    <div class="s">
      <div class="card" v-for="(profile, index) in profiles" :key="index">
        <img :src="profile.src" alt="Profile Image" class="card-img" />
        <div class="card-body">
          <h3 class="card-title">{{ profile.name }}</h3>
          <p class="card-text">{{ profile.description }}</p>
          <div class="card_buttons">
            <BButton background-color="#ebd6f7"  padding="12px 15px" border-radius="50%" >
               <PageIcons iconType="phone" color="#886cc0"></PageIcons>
            </BButton>
            <BButton background-color="#ebd6f7"  padding="12px 15px" border-radius="50%" >
               <PageIcons iconType="message" color="#886cc0"></PageIcons>
            </BButton>
            <BButton background-color="#ebd6f7"  padding="12px 15px" border-radius="50%" >
               <PageIcons iconType="video" color="#886cc0"></PageIcons>
            </BButton>
          </div>

        </div>
      </div>
    </div>
  </template>
  
  <script>
  import BButton from './BButton.vue';
  import PageIcons from './PageIcons.vue';
  export default {
    components:{
    BButton,
    PageIcons,
},
    props: {
      profiles: {
        type: Array,
        required: true,
        default: () => [
          {
            name: "Bakhdaulet Baktygaliev",
            description:
              "The name Bakdaulet is of Kazakh origin and is commonly given to boys. In Kazakh, Therefore, Bakdaulet can be interpreted to mean ",
            src: require("@/assets/a1.jpg"),
          },
        ],
      },
    },
  };
  </script>
  
  <style scoped>
  body {
    background-color: #f5f5f5;
  }
  .card {
    width: 280px;
    background-color: white;
    border-radius: 20px;
    box-shadow: 0 0 10px rgba(0, 0, 0, 0.1);
    display: flex;
    flex-direction: column;
    align-items: center;
    transition: box-shadow 0.3s ease;
  }
  .s{
    display: flex;
    gap: 20px;
    flex-wrap: wrap;
  }
  
  .card:hover {
    box-shadow: 0 0 15px rgba(0, 0, 0, 0.2);
  }
  
  .card-img {
    margin-top: 20px;
    width: 80px;
    height: 80px;
    border-radius: 50%;
    object-fit: cover;
    margin-bottom: 5px;
  }
  
  .card-body {
    width: 100%;
    padding: 20px;
    text-align: center;
  }
  
  .card-title {
    margin-bottom: 10px;
    color: #333;
  }
  
  .card-text {
    margin-bottom: 15px;
    color: #555;
  }
  .card_buttons{
    display: flex;
    align-items: center;
    gap: 5px;
  }
  </style>