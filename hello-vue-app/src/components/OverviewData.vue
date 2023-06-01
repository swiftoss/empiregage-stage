<template>
  <div class="modal-overlay" :class="{ 'modal-open': showModal }" @click="closeModal"></div>
    <div class="modal" v-show="showModal">
      <!-- Inhoud van de modal -->
    </div>
    <div class="container-data">
    <h2 class="title-tile">Taken (Vandaag)</h2>
    <div class="list" @click="openModal">
  <div class="item">
    <div class="icon-container">
  <i class="fas fa-layer-group"></i>
</div>
  </div>
  <div class="item">
    <div class="text-container">
    <div class="title-taak">Voorbeeldpagina's</div>
    <div class="date">
      17/04/23
      <span class="deadline-marker"><i class="fas fa-exclamation-circle"></i></span>
    </div>
  </div>
  </div>
  <div class="item">
<div class="circle-container">
  <div class="circle"></div>
  <div class="circle"></div>
  <div class="circle"></div>
</div>
  </div>
  <div class="item">
    <div class="progress-container">
  <span class="progress-label">Progressie</span>
  <span class="progress-percent">95%</span>
</div>
<div class="progress-container2">
  <div class="progress-bar"></div>
</div>
  </div>
  <div class="item-icon">
    <i class="fas fa-chevron-right"></i>
  </div>
</div>
<div class="divider-list"></div>
<div style="margin-top:10px;" class="list" @click="openModal">
  <div class="item">
    <div class="icon-container">
  <i class="fas fa-layer-group"></i>
</div>
  </div>
  <div class="item">
    <div class="text-container">
    <div class="title-taak">Chris prompts maken</div>
    <div class="date">
      17/04/23
      <span class="deadline-marker"><i class="fas fa-exclamation-circle"></i></span>
    </div>
  </div>
  </div>
  <div class="item">

<div class="circle-container">
  <div class="circle"></div>
  <div class="circle"></div>
  <div class="circle"></div>
</div>
  </div>
  <div class="item">
    <div class="progress-container">
  <span class="progress-label">Progressie</span>
  <span class="progress-percent">95%</span>
</div>
<div class="progress-container2">
  <div class="progress-bar"></div>
</div>
  </div>
  <div class="item-icon">
    <i class="fas fa-chevron-right"></i>
  </div>
</div>
<div class="divider-list"></div>
<div style="margin-top:10px;" class="list" @click="openModal"> 
  <div class="item">
    <div class="icon-container">
  <i class="fas fa-layer-group"></i>
</div>
  </div>
  <div class="item">
    <div class="text-container">
    <div class="title-taak">Voorbeeldpagina's</div>
    <div style="color: #757575;" class="date">
        19/04/23
    </div>
  </div>
  </div>
  <div class="item">
<div class="circle-container">
  <div class="circle"></div>
  <div class="circle"></div>
  <div class="circle"></div>
</div>
  </div>
  <div class="item">
    <div class="progress-container">
  <span class="progress-label">Progressie</span>
  <span class="progress-percent">95%</span>
</div>
<div class="progress-container2">
  <div class="progress-bar"></div>
</div>
  </div>
  <div class="item-icon">
    <i class="fas fa-chevron-right"></i>
  </div>
</div>
    </div>
  </template>
  

  <script>
    export default {
  data() {
    return {
      showModal: false
    };
  },
  methods: {
    openModal() {
      this.showModal = true;
      document.body.classList.add('modal-open');
    },
    closeModal() {
      this.showModal = false;
      document.body.classList.remove('modal-open');
    }
  }
};
  </script>
  
  
  <style scoped>
 .title-container {
  margin-left: 360px;
  margin-top: 15px;
}

.title-taak {
  font-weight: 500;
}

.item-icon{
    display: flex;
  justify-content: center;
  align-items: center;
}

.circle-container {
  display: flex;
  align-items: center;
  margin-top: 4px;
}

.circle {
  width: 35px;
  height: 35px;
  border-radius: 50%;
  background-color: #adadad;
  margin-right: -5px; /* Verwijder de standaardmarge tussen de rondjes */
}
.progress-container {
  display: flex;
  justify-content: space-between;
  align-items: center;
  margin-top: 4px;
}

.progress-label {
  margin-right: 10px;
  font-size: 14px;
}

.progress-percent {
  margin-left: 10px;
  font-size: 14px;
}

.progress-container2 {
  background-color: lightgray;
  width: 100%;
  height: 6px;
  border-radius: 8px;
  margin-top: 5px;
}

.progress-bar {
  background-color: #FF6C6C;
  width: 95%;
  height: 100%;
  border-radius: 8px;
}


.date {
  font-size: 14px;
  color: #FF6C6C;
  display: flex;
  align-items: center;
  margin-top: 1%;
}

.deadline-marker {
  margin-left: 5px;
  font-size: 16px;
}

.icon-container {
    display: flex;
  justify-content: center;
  align-items: center;
  background-color: #F37357;
  border-radius: 8px;
  padding: 10px;
  width: 22px;
  height: 22px;
}

.icon-container i {
  color: white;
}

.list {
    display: grid;
    grid-template-columns: 6% 30% 20% 30% 10%;
  gap: 10px;
  transition: background-color 0.3s ease;
  border-radius: 8px;
}

.list:hover {
  background-color: rgb(245, 245, 245); /* Stel de achtergrondkleur in voor het hover-effect */
  cursor: pointer;
}

.item {
  flex: 1;
  padding: 10px;
  margin-right: 10px;
}

.container {
  display: flex;
  align-items: center;
  justify-content: space-between;
}
.container-data {
width: 80%;
  border: 1px solid #ccc;
  padding: 20px;
  margin-left: 360px;
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

.modal-overlay {
  position: fixed;
  top: 0;
  left: 0;
  width: 100%;
  height: 100%;
  background-color: rgba(0, 0, 0, 0.5);
  z-index: 100;
  transition: opacity 0.3s ease;
  opacity: 0;
  pointer-events: none;
}

.modal-open {
  opacity: 1;
  pointer-events: auto;
}

.modal {
  position: fixed;
  top: 50%;
  left: 50%;
  transform: translate(-50%, -50%);
  width: 1000px;
  height: 600px;
  background-color: #fff;
  z-index: 101;
  border-radius: 5px;
}

.circle-button {
  width: 48px;
  height: 48px;
  border-radius: 50%;
  background-color: #F37357;
  border: none;
  box-shadow: 0 2px 4px rgba(0, 0, 0, 0.2);
  display: flex;
  align-items: center;
  justify-content: center;
  cursor: pointer;
  margin-right: 100px;
  transition: transform 0.2s ease;
}

.circle-button i {
  color: white;
  font-size: 20px;
}

.circle-button:active {
  transform: scale(0.8);
}

.title {
  font-family: "Inter", sans-serif;
  font-size: 24px;
  color: #192B31;
}

.divider {
  width: 87%;
  height: 1px;
  border-top: 1px solid #ccc;
}

.divider-list{
    width: 100%;
  height: 1px;
  border-top: 1px solid #ccc;
  margin-top: 15px;
}

  </style>