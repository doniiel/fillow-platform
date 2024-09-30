<template>
<div class="messgaebh_main">
    <div class="left_board">
        <div>
            <BButton padding="10px 15px" border-radius="50%" background-color="#886cc0">
            <PageIcons iconType="f" color="white" background-color="#886cc0" class="circle"></PageIcons>
            </BButton>
        </div>
       
        <div class="left_text">
            <ContentTitle color="#312A2A" fontSize="16px">Filow Designer Team</ContentTitle>
            <ContentTitle color="#9DA1A5" fontSize="13px">We share about daily life as designer in the world</ContentTitle>
        </div>
           </div>

    <div class="right_board">
        <MessageToolbar></MessageToolbar>
    </div>
  
</div>
</template>

<script>
import MessageToolbar from './MessageToolbar.vue';
import PageIcons from './PageIcons.vue';
import BButton from './BButton.vue';
import ContentTitle from './ContentTitle.vue';

export default{
   components:{
    PageIcons,
    BButton,
    ContentTitle,
    MessageToolbar,
}
}

</script>

<style scoped>
.messgaebh_main{
    display: flex;
    align-items: center;
}
.left_board{
    display: flex;
    align-items: center;
}
.left_text{
    text-align: left;
}

</style>