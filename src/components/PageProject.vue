<template>
  <div class="project">
    <div class="pcard">
        <PCard :profiles ="sampleProfiles"></PCard>
    </div>
    <div class="nav_card">
      <div>
        <ContentTitle fontSize="14px" color="#312a2a">Showing 5 from 102 data</ContentTitle>
      </div> 
         <NavPagination></NavPagination>
    </div>
  </div>
</template>

<script>
import PCard from './PCard.vue'
import NavPagination from './NavPagination.vue';
import ContentTitle from './ContentTitle.vue';
export default{
    components:{
       PCard,
       NavPagination,
       ContentTitle,

    },
    data(){
        return{
        sampleProfiles: [
        {
          id: '#P-000441425',
          project:'Redesign Owlio Landing Page Web..',
          dateSent:'Created on Sep 8th, 2020',
          srcClient: require("@/assets/z1.jpg"),
          nameClient: "James Jr.",
          srcPerson: require("@/assets/z2.jpg"),
          namePerson: 'Marley Dokidis',
          date: 'Tuesday, Sep 29th 2020',
          label : 'pending',
        },
        {
          id: '#P-000441425',
          project:'Create UseCase Diagram of Fillow..',
          dateSent:'Created on Sep 8th, 2020',
          srcClient: require("@/assets/z3.jpg"),
          nameClient: "Jakob Vetrovs",
          srcPerson: require("@/assets/z4.jpg"),
          namePerson: 'Marley Dokidis',
          date: 'Tuesday, Sep 29th 2020',
          label : 'progress',
        },
        {
          id: '#P-000441425',
          project:'Redesign Owlio Landing Page Web..',
          dateSent:'Created on Sep 8th, 2020',
          srcClient: require("@/assets/z1.jpg"),
          nameClient: "James Jr.",
          srcPerson: require("@/assets/z2.jpg"),
          namePerson: 'Marley Dokidis',
          date: 'Tuesday, Sep 29th 2020',
          label : 'closed',
        },
        {
          id: '#P-000441425',
          project:'Create UseCase Diagram of Fillow..',
          dateSent:'Created on Sep 8th, 2020',
          srcClient: require("@/assets/z3.jpg"),
          nameClient: "Jakob Vetrovs",
          srcPerson: require("@/assets/z4.jpg"),
          namePerson: 'Marley Dokidis',
          date: 'Tuesday, Sep 29th 2020',
          label : 'progress',
        },
        {
          id: '#P-000441425',
          project:'Redesign Owlio Landing Page Web..',
          dateSent:'Created on Sep 8th, 2020',
          srcClient: require("@/assets/z1.jpg"),
          nameClient: "James Jr.",
          srcPerson: require("@/assets/z2.jpg"),
          namePerson: 'Marley Dokidis',
          date: 'Tuesday, Sep 29th 2020',
          label : 'pending',
        },
    ]
        }
    },
    
}
</script>

<style scoped>
 .project{
    padding: 20px;
 }
</style>