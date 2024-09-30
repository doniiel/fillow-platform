<template>
  <div class="general">
    <div class="leftContent">
       <SliderBar @itemClick="handleSliderBarItemClick"></SliderBar>
    </div>

   <div class="rightContent"> 
     <div> 
        <PageHeaders></PageHeaders>
     </div>

      <div class="content_wrapper" v-if="element == 'Apps' ">
        <div class="left_content_wrap"><PageMessageUsers></PageMessageUsers></div>
        <div class="right_content_wrap"><MessageBoardInputs></MessageBoardInputs></div>
    </div>
    <PageContacts v-if="element == 'Charts'"></PageContacts>
    <PageProject v-if="element== 'Bootstrap'"></PageProject>
    <PageKanban v-if="element== 'Plugins'"></PageKanban>

   </div> 
  </div>
  <PageFooter></PageFooter>
</template>

<script>
import PageHeaders from './components/PageHeaders.vue'
import PageMessageUsers from './components/PageMessageUsers.vue'
import MessageBoardInputs from './components/MessageBoardInputs.vue'
import PageFooter from './components/PageFooter.vue'
import SliderBar from './components/SliderBar.vue'
import PageContacts from './components/PageContacts.vue'
import PageProject from './components/PageProject.vue'
import PageKanban from './components/PageKanban.vue'

export default {
  name: 'App',
  components: {
    PageHeaders,
    PageMessageUsers,
    MessageBoardInputs,
    PageFooter,
    SliderBar,
    PageContacts,
    PageProject,
    PageKanban,
},
  data(){
    return {
      element: 'Apps',
    }
  },
  methods: {
    toggleDrawer() {
      this.$refs.drawer.toggleDrawer();
    },
    handleSliderBarItemClick(value) {
      console.log('Item clicked in App.vue:', value);
      this.element = value;
    },
 },
}
</script>

<style>

*{
  margin: 0;
  padding: 0;
  box-sizing: border-box;
}
.general{
  display: flex;
}
.leftContent{
  width: 20%;
  background-color: #ffffff;
}
#app {
  font-family: Avenir, Helvetica, Arial, sans-serif;
  -webkit-font-smoothing: antialiased;
  -moz-osx-font-smoothing: grayscale;
  text-align: center;
  color: #2c3e50;
  background-color: #f3ebf6;
}
.search{
  padding: 50px;
}

.content_wrapper{
  display: flex;
  padding:30px;
}
.left_content_wrap{
  width: 120%;
}
.rightContent{
  width: 120%;
  height: 100%;
}
</style>
