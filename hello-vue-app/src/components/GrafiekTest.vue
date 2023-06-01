<template>

    <div class="container-data">
    <h2 class="title-tile">Omzet</h2>
    <div class="grafiek">
      <div v-for="item in data" :key="item.id" class="staaf-wrapper">
        <div
          class="staaf"
          :style="{ height: item.value + 'px' }"
          @mouseover="showTooltip(item.id)"
          @mouseout="hideTooltip"
        >
          <div class="tooltip" v-show="item.showTooltip">
            <p>Omzet:</p>
            <div class="tooltip-value">{{ item.value }}</div>
          </div>
        </div>
        <div class="maand">{{ item.month }}</div>
      </div>
    </div>
    </div>
  </template>
  
  <script>
  export default {
    data() {
      return {
        data: [
          { id: 1, value: 150, showTooltip: false, month: 'Jan' },
          { id: 2, value: 250, showTooltip: false, month: 'Feb' },
          { id: 3, value: 170, showTooltip: false, month: 'Mar' },
          { id: 4, value: 150, showTooltip: false, month: 'Apr' },
          { id: 5, value: 200, showTooltip: false, month: 'Mei' }
        ]
      };
    },
    methods: {
      showTooltip(itemId) {
        this.data.forEach(item => {
          item.showTooltip = item.id === itemId;
        });
      },
      hideTooltip() {
        this.data.forEach(item => {
          item.showTooltip = false;
        });
      }
    }
  };
  </script>
  
  <style>
  .grafiek {
    display: flex;
    align-items: flex-end;
    height: 300px;
  }
  
  .container-data {
    width: 37%;
  border: 1px solid #ccc;
  padding: 20px;
  margin-left: 229px;
  position: relative;
  border-radius: 8px;
  margin-top: 40px;
  font-family: "Inter", sans-serif;
}

.title-tile {
    background-color: white;
  padding: 5px 10px;
  position: absolute;
  top: -29px;
  left: 10px;
  font-size: 15px;
  font-family: "Inter", sans-serif;
  font-weight: 500;
}

  .staaf-wrapper {
    display: flex;
    flex-direction: column;
    align-items: center;
    margin-left: 25px;
  }
  
  .staaf {
    width: 40px;
    background-color: #f37357;
    border-radius: 5px;
    position: relative;
    cursor: pointer;
  }
  
  .tooltip {
    position: absolute;
    left: 50%;
    transform: translateX(-50%);
    background-color: #fff;
    box-shadow: 0 2px 4px rgba(0, 0, 0, 0.2);
    padding: 15px;
    border-radius: 8px;
    font-size: 15px;
    z-index: 999;
    font-family: 'Inter', sans-serif;
    font-weight: 600;
  }
  
  .tooltip p {
    margin-bottom: 5px;
    font-weight: 500;
    margin-top: 0;
  }
  
  .maand {
    text-align: center;
    font-size: 13px;
    margin-top: 8px;
    font-family: 'Inter', sans-serif;
  }
  </style>
  