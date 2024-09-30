<template>
  <div class="Sliderbar">
    <SliderBarLogo></SliderBarLogo>
    <SliderBarItems :items="sliderItems"   @itemClick="handleItemClick"></SliderBarItems>
    <div class="end"><SliderBarFooter></SliderBarFooter></div>
  </div>
</template>
<script>
import SliderBarLogo from'./SliderBarLogo.vue';
import SliderBarItems from './SliderBarItems.vue';
import SliderBarFooter from './SliderBarFooter.vue';
 export default{
    components:{
      SliderBarLogo,
      SliderBarItems,
      SliderBarFooter
    },
    data(){
      return{
        sliderItems: [
        { label: "Apps" , icon: "info" },
        { label: "Charts" ,icon :"chart"},
        { label: "Bootstrap" ,icon: "bootstrap"},
        { label: "Plugins" ,icon: "heart"},
        { label: "Widget" ,icon: "user"},
        { label: "Forms" ,icon: "file"},
        { label: "Table" ,icon: "table"},
        { label: "Pages" ,icon: "clone"},
      ],

      }

    },
    methods: {
      handleItemClick(value) {
      console.log('Item clicked in SliderBar.vue:', value);
      this.$emit('itemClick', value);
    },
  }
 }
</script>

<style scoped>
.sliderbar{
    background-color: white;
    position: fixed;
}
.end{
  justify-content: end;
}

</style>