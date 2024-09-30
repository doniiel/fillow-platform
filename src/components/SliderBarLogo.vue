<template>
    <div class="logo">
        <div>
            <BButton padding="10px 15px" border-radius="50%" background-color="#886cc0">
               <PageIcons iconType="f" color="white" background-color="#886cc0" class="circle"></PageIcons>
            </BButton>
        </div>
       
        <div class="left_text">
            <ContentTitle fontSize="25px" color="#886cc0" fontWeight="900">Fillow</ContentTitle>
            <ContentTitle fontSize="11px">Saas Admin Dashboard</ContentTitle>
        </div>
    </div>
</template>

<script>
import ContentTitle from './ContentTitle.vue';
import BButton from './BButton.vue';
import PageIcons from './PageIcons.vue';
export default{
  components:{
    ContentTitle,
    BButton,
    PageIcons,
  }
}
</script>

<style scoped>
.logo{
    background-color: #e9e2f8;
    padding: 6px 18px;
    display: flex;
    align-items: center;
}

</style>