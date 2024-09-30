<template>
    <div class="kanban_header">
        <div class="left_pos">
        
        <div class="text">
            <div class="Title">
                <ContnetTitle fontSize="30px" fontWeight="800">Fillow Company Profile Website Phase 1</ContnetTitle> 
                <div class="s">
                    <ContentTitle fontSize="14px" color="#9da1a5">Created</ContentTitle>
                    <ContentTitle fontSize="14px" color="#312a2a">Hajime Mahmuden</ContentTitle>
                    <ContentTitle fontSize="14px" color="#9da1a5">on June 31, 2020</ContentTitle>
                </div>
            </div>
        </div>
        <div>
            <div class="Users_cont">
            <div class="photo">
                <UserPortfolio :profileImage="require('@/assets/a3.jpg')" width="50" height="50"></UserPortfolio>
                <UserPortfolio :profileImage="require('@/assets/a4.jpg')" width="50" height="50"></UserPortfolio>
                <UserPortfolio :profileImage="require('@/assets/a1.jpg')" width="50" height="50"></UserPortfolio>
                <UserPortfolio :profileImage="require('@/assets/a2.jpg')" width="50" height="50"></UserPortfolio>
            </div>
            <div class="Btns">
                <BButton backgroundColor="#886cc0" color="white">Invite People</BButton>
                <BButton backgroundColor="#886cc0" color="white">Edit</BButton>
                <BButton backgroundColor="#886cc0" color="white">Private</BButton>
            </div>
           </div>
        </div>
    </div>
        <div class="right_pos">
            <div class="top_container">
            <div>
                <ContentTitle fontSize="14px" color="#9da1a5">Fillow Studios</ContentTitle>
               <ContentTitle fontSize="14px" color="#9da1a5">Software House</ContentTitle>
            </div>
             <BButton backgroundColor="#886cc0" padding="10px 15px" borderRadius="50%">
                <PageIcons iconType="f" color="white"></PageIcons>
             </BButton>
            </div>

                <ContentTitle fontSize="14px">Total Progress 60%</ContentTitle>
             <ConProgressbar progressBarColor="#886cc0" percentage="60"></ConProgressbar>
        </div>
    </div>
</template>

<script>
import PageIcons from './PageIcons.vue';
import BButton from './BButton.vue';
import ConProgressbar from './ConProgressbar.vue';
import ContentTitle from './ContentTitle.vue';
import UserPortfolio from './UserPortfolio.vue';
export default{
    
    components: { 
        ContentTitle,
        UserPortfolio,
       BButton,
        ConProgressbar, 
        PageIcons,
     }
}
</script>

<style scoped>
.kanban_header{
    background-color: #ffffff;
    padding: 20px;
    display: flex;
    justify-content: space-between;
    border-radius: 20px;
}
.text{
    display: flex;
    gap: 10px;
    align-items: center;
}
.photo{
    display: flex;
    align-items: center;
}
.Btns{
 display: flex;
 align-items: center;
}
.Users_cont{
    display: flex;
    align-items: center;
}
.top_container{
    display: flex;
    align-items:center ;
}
.title{
    display: flex;
    align-items: center;
}
.s{
    margin-top: 10px;
    display: flex;
    gap: 10px;
    align-items: center;
}

</style>