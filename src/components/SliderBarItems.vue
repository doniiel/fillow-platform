<template>
      <div v-for="(item, index) in items" :key="index" class="slider-item">
        <BButton backgroundColor="white" color="#737b8b" gap="30px" @buttonClick="setData(item.label)" :value="item.label">
            <PageIcons :iconType="item.icon" color="#737b8b"></PageIcons>
            <p>{{ item.label }}</p></BButton>
      </div>
  </template>
  
  <script>
import BButton from './BButton.vue';
import PageIcons from './PageIcons.vue';

  export default {
    components:{
       BButton, 
       PageIcons,
    },
    props: {
        items: {
            type: Array,
            required: true
        },
        itemClick: {
            type: Function,
            default: () => { }
        }
    },
    methods: {
    setData(value) {
      this.$emit('itemClick', value); 
    },
  },
};
  </script>
  
  <style scoped>

  </style>