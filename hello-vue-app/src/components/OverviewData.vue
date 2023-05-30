<template>
    <div class="title-container">
    <div class="container">
    <h1 class="title">Overview</h1>
    <button class="circle-button" @click="openModal">
      <i class="fas fa-plus"></i>
    </button>
    <div class="modal-overlay" :class="{ 'modal-open': showModal }" @click="closeModal"></div>
    <div class="modal" v-show="showModal">
      <!-- Inhoud van de modal -->
    </div>
     </div>
    <div class="divider"></div>
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
  margin-left: 350px;
  margin-top: 40px;
}

.container {
  display: flex;
  align-items: center;
  justify-content: space-between;
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
  width: 500px;
  height: 300px;
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
  </style>