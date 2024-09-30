<template>
    <div class="pagemessgae_main">
        <div class="header">
            <div class="header_container">
            <div class="texts">
            <ContentTitle color="black" fontSize="21px" fontWeight="bold">Inbox</ContentTitle>
            <ContentTitle color="#737b8b" fontSize="13px" fontWeight="600">(2,456)</ContentTitle>
            </div>
             <BButton  color="#fff"
                        background-color="#886cc0"
                        border-radius="20px"
                        padding="5px 8px"
                        border-size="0px" >
                <PageIcons iconType="plus" color="white"></PageIcons>
             </BButton>
            </div>
        <div>
            <GButton :val="status2" :items="items1" @change-status="status2 = $event"></GButton>
        </div>
    </div>

    <div class="team">
        <ContentTitle color="#9da1a5" fontSize="12px" fontWeight="400">TEAM</ContentTitle>
    </div>
    <messageUserItem
   :imgSrc="users"
    content-title="Follow Designer Team"
   content-description="Hey Jenny, don`t forget to prepare prototype for next week"
   content-time="2m ago"
   width="30"
   height="30"></messageUserItem>

   <messageUserItem
   :imgSrc="users"
    content-title="Follow Designer Team"
   content-description="Hey Jenny, don`t forget to prepare prototype for next week"
   content-time="2m ago"
   width="30"
   height="30"></messageUserItem>
   <div class="team">
        <ContentTitle color="#9da1a5" fontSize="12px" fontWeight="400">RECENT MESSAGE</ContentTitle>
        <BButton  color="#fff"
                        background-color="white"
                        border-radius="20px"
                        padding="5px 8px"
                        border-size="0px" >
                <PageIcons iconType="dots" color="#9da1a5"></PageIcons>
             </BButton>
    </div>
    <messageUserItem
   :imgSrc="users1"
    content-title="Rayna Carder"
    content-description="I remember that project due is tomorrow."
    content-time="2m ago"
    width="50"
    height="50"></messageUserItem>
    <messageUserItem
   :imgSrc="users2"
    content-title="Rayna Carder"
    content-description="I remember that project due is tomorrow."
    content-time="2m ago"
    width="50"
    height="50"></messageUserItem>
    <messageUserItem
   :imgSrc="users3"
    content-title="Rayna Carder"
    content-description="I remember that project due is tomorrow."
    content-time="2m ago"
    width="50"
    height="50"></messageUserItem>
    <messageUserItem
   :imgSrc="users3"
    content-title="Rayna Carder"
    content-description="I remember that project due is tomorrow."
    content-time="2m ago"
    width="50"
    height="50"></messageUserItem>



    </div>
</template>

<script>
import ContentTitle from './ContentTitle.vue'
import BButton from './BButton.vue'
import PageIcons from './PageIcons.vue';
import GButton from './GButton.vue';
import MessageUserItem from './MessageUserItem.vue';


 export default{
    components:{
    ContentTitle,
    BButton,
    PageIcons,
    GButton,
    MessageUserItem,
},
data(){
    return{
        status2:0,
        items1: [
        {
          status: 0,
          title: "All",
          class: "btn-default",
        },
        {
          status: 1,
          title: "Recent",
          class: "btn-success",
        },
        {
          status: 2,
          title: "Message",
          class: "btn-danger",
        },
      ],
      users: [
       { userImages: require('@/assets/a1.jpg') },
       { userImages: require('@/assets/a2.jpg') },
       { userImages: require('@/assets/a3.jpg') },
       { userImages: require('@/assets/a4.jpg') },
      ],
      users1: [
      { userImages: require('@/assets/a5.jpg') },
      ],
      users2: [
      { userImages: require('@/assets/a6.jpg') },
      ],
      users3: [
      { userImages: require('@/assets/a7.jpg') },
      ],

    } 
},
methods: {
    toggleAccordionItem(index) {
      this.accordionItems[index].isOpen = !this.accordionItems[index].isOpen;
    },
  },
    
 }
</script>

<style scoped>
.pagemessgae_main{
    padding: 2px;
    background-color: #fff;
    border-right: 1px solid #d6dadd;
    border-radius: 10px 0 0 10px;
    height: 100%;
}
.header{
    padding: 30px 16px;
}
.header_container{
    display: flex;
    align-items: center;
    justify-content: space-between;
}
.texts{
    align-items: center;
    display: flex;
    gap:12px;
}
.team{
    display: flex;
    align-items: center;
    justify-content: space-between;
    padding: 10px 15px;
}
</style>
