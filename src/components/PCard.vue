<template>
    <div class="s">
        <div class="card_header">
            <div>
                <GButton :val="status2" :items="items1" @change-status="status2 = $event" ></GButton>
            </div>
            <div>
                <BButton color="white" background-color="#886cc0" borderRadius="30px" padding="10px 15px">
                   <PageIcons iconType="plus" color="white"></PageIcons>
                   <p>New Contact</p>
              </BButton>
            </div>
        </div>


        <div class="card" v-for="(profile, index) in filteredProfiles" :key="index">
        <div>
            <ContentTitle color="#886cc0" fontSize="14px">{{profile.id }}</ContentTitle>
            <ContentTitle color="#312a2a" fontSize="15px" fontWeight="700">{{ profile.project }}</ContentTitle>
            <ContentTitle color="#9dA1a5" fontSize="14px">{{ profile.dateSent }}</ContentTitle>
        </div>
        <div class="human">
            <UserPortfolio :profileImage="profile.srcClient" alt="Profile Image" class="card-img" width="45" height="45"></UserPortfolio>
            <div>
                <ContentTitle color="#9dA1a5" fontSize="14px" fontWeight="400">Client</ContentTitle>
                <ContentTitle color="#312a2a" fontSize="15px" fontWeight="700">{{ profile.nameClient}}</ContentTitle>
            </div>
        </div>
        <div class="human">
            <UserPortfolio :profileImage="profile.srcPerson" alt="Profile Image" class="card-img" width="45" height="45"></UserPortfolio>
            <div>
                <ContentTitle color="#9dA1a5" fontSize="14px">Person in charge</ContentTitle>
                <ContentTitle color="#312a2a" fontSize="15px" fontWeight="700">{{ profile.namePerson}}</ContentTitle>
            </div>
        </div>
        <div class="human">
            <BButton backgroundColor="#886cc0" borderRadius="50%" padding="10px 15px">
            <PageIcons iconType="storm" color="white"></PageIcons>
            </BButton>
            <div>
                <ContentTitle color="#9dA1a5" fontSize="14px">Decline</ContentTitle>
                <ContentTitle color="#312a2a" fontSize="15px" fontWeight="700">{{ profile.date}}</ContentTitle>
            </div>
        </div>
        
        <div class="human">
            <div>
                <VLabels :labelType="profile.label"></VLabels>
            </div>
            <div class="labels">
                <PageIcons iconType="dot"></PageIcons>
            </div>
        </div>


            
          </div>
    </div>
  </template>
  
  <script>
  import PageIcons from './PageIcons.vue';
  import BButton from './BButton.vue';
  import ContentTitle from './ContentTitle.vue';
  import UserPortfolio from './UserPortfolio.vue';
  import VLabels from './VLabels.vue'
  import GButton from './GButton.vue';


  export default {
    components:{
    ContentTitle,
    UserPortfolio,
    BButton,
    PageIcons,
    VLabels,
    GButton,
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
    data(){
        return{
            status2:0,
        items1: [
        {
          status: 0,
          title: "All Status",
          class: "btn-default",
        },
        {
          status: 1,
          title: "Progress",
          class: "btn-success",
        },
        {
          status: 2,
          title: "Pending",
          class: "btn-danger",
        },
        {
          status: 3,
          title: "closed",
          class: "btn-danger",
        },

              ]
        }
    },
    computed: {
    filteredProfiles() {
      if (this.status2 === 0) {
        return this.profiles;
      } else {
        const statusFilter = this.items1.find(item => item.status === this.status2);
        if (statusFilter) {
          return this.profiles.filter(profile => profile.label === statusFilter.title.toLowerCase());
        } else {
          return [];
        }
      }
    },
  },
  methods: {
    changeStatus(newStatus) {
      this.status2 = newStatus;
    },
    toggleAccordionItem(index) {
      this.accordionItems[index].isOpen = !this.accordionItems[index].isOpen;
    },
  },
};
  </script>
  
  <style scoped>
.card {
  display: flex;
  flex-wrap: wrap;
  justify-content: space-between;
  background-color: #fff;
  padding: 20px;
  gap: 50px; 
  border-radius: 10px;
  margin-bottom: 20px;
}
.card_header{
    display: flex;
    align-items: center;
    justify-content: space-between;
}
.human, .labels {
    align-items: center;
    display: flex;
  flex: 1; 
}



 
  </style>