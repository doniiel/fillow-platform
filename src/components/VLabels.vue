<template>
    <div>
      <div class="label-container">
        <span class="label" :class="getLabelClass(labelType)">
          {{ getLabelText(labelType) }}
        </span>
      </div>
    </div>
  </template>
  
  <script>
  export default {
    props: {
      labelType: {
        type: String,
        required: true,
      },
    },
    methods: {
      getLabelText(type) {
        switch (type.toLowerCase()) {
          case '':
            return 'Default';
          case 'primary':
            return 'Primary';
          case 'success':
            return 'Success';
          case 'progress':
            return 'On Progress';
          case 'pending':
            return 'Pending';
          case 'closed':
            return 'Closed';
          default:
            return '';
        }
      },
      getLabelClass(type) {
        return `label label-${type.toLowerCase()}`;
      },
    },
  };
  </script>
  
  <style scoped>
  body {
    background-color: #f5f5f5;
  }
  
  .label-container {
    margin: 0 auto;
    padding: 10px;
    border-radius: 10px;
    display: flex;
    justify-content: space-around;
    align-items: center;
    flex-wrap: wrap;
  }
  
  .label {
    box-shadow: 0 0 10px rgba(0, 0, 0, 0.3);
    padding: 5px 10px;
    margin: 2px;
    border-radius: 25px;
    display: inline-block;
    transition: background-color 0.3s ease, color 0.3s ease, transform 0.2s ease;
  }
  
  .label:hover {
    background-color: #333;
    color: #fff;
    transform: scale(1.05);
  }
  
  .label-default {
    background-color: #f5f5f5;
    color: #666;
  }
  
  .label-primary {
    background-color: #6699cc;
    color: white;
  }
  
  .label-success {
    background-color: #99cc66;
    color: white;
  }
  
  .label-progress {
    background-color: #99cc66;
    color: white;
  }
  
  .label-pending {
    background-color: yellow;
    color: #333;
  }
  
  .label-closed {
    background-color: red;
    color: white;
  }
  </style>