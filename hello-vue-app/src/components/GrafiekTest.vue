<template>
    <div class="grafiek">
      <div v-for="item in data" :key="item.id" class="staaf" :style="{ height: item.value + '%' }"></div>
    </div>
  </template>
  
  <script>
  export default {
    data() {
      return {
        data: [
          { id: 1, value: 80 },
          { id: 2, value: 50 },
          { id: 3, value: 70 },
          { id: 4, value: 60 },
          { id: 5, value: 90 }
        ]
      };
    }
  };
  </script>
  
  <style>
  .grafiek {
    display: flex;
    align-items: flex-end;
    height: 300px;
    margin-left: 350px;
  }
  
  .staaf {
    width: 30px;
    background-color: #F37357;
    margin-right: 10px;
    border-radius: 5px;
  }
  </style>