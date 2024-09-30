<template>
  <div class="Contact">
      <div class="con_header">
        <div>
         <SearchBar></SearchBar>
        </div>
         <BButton color="white" background-color="#886cc0" borderRadius="30px" padding="10px 15px">
            <PageIcons iconType="plus" color="white"></PageIcons>
            <p>New Contact</p>
         </BButton>
      </div>

    <div class="cards">
        <CCard :profiles="sampleProfiles"></CCard>
    </div>

    <div class="nav_card">
      <div>
        <ContentTitle fontSize="14px" color="#312a2a">Showing 10 from 160 data</ContentTitle>
      </div> 
         <NavPagination></NavPagination>
    </div>
  </div>
</template>

<script>
import BButton from './BButton.vue';
import CCard from './CCard.vue';
import ContentTitle from './ContentTitle.vue';
import NavPagination from './NavPagination.vue'
import SearchBar from './SearchBar.vue';
import PageIcons from './PageIcons.vue';
export default{
  components:{
    CCard,
    ContentTitle,
    NavPagination,
    SearchBar,
    BButton,
    PageIcons,
},
data() {
    return {
      sampleProfiles: [
        {
          name: "Jakob Gouse",
          description: "Highspeed Inc.",
          src: require("@/assets/pic1.jpg"),
        },
        {
          name: "Gretchen Aminoff",
          description: "Redblue Studios",
          src: require("@/assets/pic2.jpg"),
        },
        {
          name: "Davis Siphron",
          description: "Beep Beep Inc.",
          src: require("@/assets/pic3.jpg"),
        },
        {
          name: "Zaire Lubin",
          description: "Highspeed Inc.",
          src: require("@/assets/pic4.jpg"),
        },
        {
          name: "Jakob Gouse",
          description: "Highspeed Inc.",
          src: require("@/assets/pic1.jpg"),
        },
        {
          name: "Gretchen Aminoff",
          description: "Redblue Studios",
          src: require("@/assets/pic2.jpg"),
        },
        {
          name: "Davis Siphron",
          description: "Beep Beep Inc.",
          src: require("@/assets/pic3.jpg"),
        },
        {
          name: "Zaire Lubin",
          description: "Highspeed Inc.",
          src: require("@/assets/pic4.jpg"),
        },
        {
          name: "Jakob Gouse",
          description: "Highspeed Inc.",
          src: require("@/assets/pic1.jpg"),
        },
        {
          name: "Gretchen Aminoff",
          description: "Redblue Studios",
          src: require("@/assets/pic2.jpg"),
        },
        {
          name: "Davis Siphron",
          description: "Beep Beep Inc.",
          src: require("@/assets/pic3.jpg"),
        },
        {
          name: "Zaire Lubin",
          description: "Highspeed Inc.",
          src: require("@/assets/pic4.jpg"),
        },

      ],
    }
 }
}
</script>

<style>
.con_header{
    display: flex;
    justify-content: space-between;
}
.Contact{
    width: 100%;
    height: 100%;
    padding:30px 40px;
}
.nav_card{
    margin-top: 30px;
    display: flex;
    align-items: center;
    justify-content: space-between;
}

</style>