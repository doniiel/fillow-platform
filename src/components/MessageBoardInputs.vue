<template>
  <div class="main">
       <MessageBoardHeader></MessageBoardHeader>
       <div class="mes_cont">
        <MessageBoardItem :messageItem="message1" :profileImage="require('@/assets/a8.jpg')"></MessageBoardItem>
       <MessageBoardItem :messageItem="message2" :profileImage="require('@/assets/a8.jpg')"></MessageBoardItem>
       <MessageBoarUserItem :messageItem="message3" :profileImage="require('@/assets/user.jpg')"></MessageBoarUserItem>
       <MessageBoarUserItem :messageItem="message4" :profileImage="require('@/assets/user.jpg')"></MessageBoarUserItem>
       <MessageBoardItem :messageItem="message2" :profileImage="require('@/assets/a8.jpg')"></MessageBoardItem>
        </div>
        <FTextArea></FTextArea>
        <div class="buttons">
          <div class="left_buttons">
          <BButton><PageIcons iconType="left" color="#9Da1a5"></PageIcons></BButton>
          <BButton><PageIcons iconType="right" color="#9Da1a5"></PageIcons> </BButton>
          <BButton><PageIcons iconType="t" color="#9Da1a5"></PageIcons></BButton>
          <BButton><PageIcons iconType="b" color="#9Da1a5"></PageIcons></BButton>
          <BButton><PageIcons iconType="i" color="#9Da1a5"></PageIcons> </BButton>
        </div>
        <div class="right_buttons">
          <BButton><PageIcons iconType="smile" color="#886CC0"></PageIcons></BButton>
          <BButton><PageIcons iconType="paperclip" color="#886CC0"></PageIcons></BButton>
          <BButton backgroundColor="#886CC0" color="white"><PageIcons iconType="plane" color="white"></PageIcons><p>Send</p></BButton>
        </div>
        </div>
       </div>
      
</template>

<script>
import MessageBoardHeader from './MessageBoardHeader.vue';
import MessageBoardItem from './MessageBoardItem.vue';
import MessageBoarUserItem from './MessageBoardUserItem.vue';
import FTextArea from './FTextArea.vue'
import BButton from './BButton.vue';
import PageIcons from './PageIcons.vue';

export default{
  components:{
    MessageBoardHeader,
    MessageBoardItem,
    MessageBoarUserItem,
    FTextArea,
    BButton,
    PageIcons,
  
},
  data(){
    return{
      message1: {
        dateSent: "Sunday, October 24th, 2020 at 4.30 AM",
        userMessage: "Sed ut perspiciatis unde omnis iste natus error sit voluptatem accusantium doloremque laudantium, totam rem aperiam, eaque ipsa quae ab illo inventore veritatis et quasi architecto beatae vitae dicta sunt explicabo. Nemo enim ipsam voluptat"
      },
      message2: {
        dateSent: "Sunday, October 24th, 2020 at 4.30 AM",
        userMessage: "Hey, check my design update last night. Tell me what you think and if that is OK"
      },
      message3: {
        dateSent: "9.30 AM",
        userMessage: "sed quia consequuntur magni dolores eos qui ratione voluptatem sequi nesciunt. Neque porro quisquam est, qui dolorem ipsum quia dolor sit amet"
      },
      message4: {
        dateSent: "9.30 AM",
        userMessage: "sed quia consequuntur magni dolores eos qui ratione voluptatem sequi nesciunt. Neque porro quisquam est, qui dolorem ipsum quia dolor sit amet"
      },
    }
  }
}
</script>

<style scoped>
.main{
  padding: 0 30px;
  background-color: rgb(255, 255, 255);
  border-radius: 0 10px 10px 0;
  padding-bottom: 60px;
}
.mes_cont{
  border-top: 1px solid #d6dadd;
}
.left_buttons{
  display: flex;
  align-items: center;
}
.right_buttons{
  display: flex;
  align-items: center;
}
.buttons{
  display: flex;
  align-items: center;
  justify-content: space-between;
}
</style>
