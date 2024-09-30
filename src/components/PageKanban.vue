<template>
       
  <div class="kanban">
    <div>
      <KanbanHeader></KanbanHeader>
    </div>
    <div class="kanban_container">
      <KCard :cards="content" title="To-do list(2)"></KCard>
      <KCard :cards="content2" title="Done(3)"></KCard>
      <KCard :cards="content3" title="On Progress"></KCard>
      <KCard :cards="content4" title="Done"></KCard>
    </div>
  </div>
</template>

<script>
import KCard from './KCard.vue'
import KanbanHeader from './KanbanHeader.vue'
export default{
    components:{
        KCard,
        KanbanHeader,
    },
    data(){
        return{
            content:[
            {
          title: 'Designer',
          titleColor: '#ffA7D7',
          description: 'Create wireframe for landing page phase 1',
          percentage: 40,
          progressBarColor: '#ffA7D7',
          userSrc: require('@/assets/a1.jpg'),
          date: 'Due in 4 days',
        },
        {
          title: 'Iportant',
          titleColor: '#ffbf00',
          description: 'Visual Graphic for Presentation to client',
          percentage: 40,
          progressBarColor: '#ffbf00',
          userSrc: require('@/assets/a2.jpg'),
          date: 'Due in 4 days',
        },
            ],


            content2:[
            {
          title: 'Bugs Fixing',
          titleColor: '#fc2e53',
          description: 'Update Information in footer section',
          percentage: 20,
          progressBarColor: '#fc2e53',
          userSrc: require('@/assets/a1.jpg'),
          date: 'Due in 4 days',
        },
        {
          title: 'Bugs Fixing',
          titleColor: '#fc2e53',
          description: 'Update Information in footer section',
          percentage: 30,
          progressBarColor: '#fc2e53',
          userSrc: require('@/assets/a2.jpg'),
          date: 'Due in 4 days',
        },
        {
          title: 'Html',
          titleColor: '#ffa7d7',
          description: 'Create wireframe for loading page phase 1',
          percentage: 40,
          progressBarColor: '#ffa7d7',
          userSrc: require('@/assets/a3.jpg'),
          date: 'Due in 4 days',
        },
            ],
            content3:[
            {
          title: 'Update',
          titleColor: '#09BD3C',
          description: 'Update Information in footer section',
          percentage: 100,
          progressBarColor: '#09BD3C',
          userSrc: require('@/assets/a1.jpg'),
          date: 'Due in 4 days',
        },
        {
          title: 'Vidoe',
          titleColor: '#d653c1',
          description: 'Update Information in footer section',
          percentage: 80,
          progressBarColor: '#d653c1',
          userSrc: require('@/assets/a1.jpg'),
          date: 'Due in 4 days',
        },
            ],
            content4:[
            {
          title: 'Bugs Fixing',
          titleColor: '#fc2e53',
          description: 'Update Information in footer section',
          percentage: 100,
          progressBarColor: '#fc2e53',
          userSrc: require('@/assets/a1.jpg'),
          date: 'Due in 4 days',
        },
        {
          title: 'Bugs Fixing',
          titleColor: '#fc2e53',
          description: 'Update Information in footer section',
          percentage: 100,
          progressBarColor: '#fc2e53',
          userSrc: require('@/assets/a1.jpg'),
          date: 'Due in 4 days',
        },
        {
          title: 'Html',
          titleColor: '#ffa7d7',
          description: 'Create wireframe for loading page phase 1',
          percentage: 100,
          progressBarColor: '#ffa7d7',
          userSrc: require('@/assets/a1.jpg'),
          date: 'Due in 4 days',
        },
            ],

        }
    }
}

</script>

<style scoped>
.kanban{
    align-items: center;
    padding: 20px;
}
.kanban_container{
  display: flex;
}

</style>