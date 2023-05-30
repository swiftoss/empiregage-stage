<template>
    <header class="header">
      <div class="header-left">
        <h1 class="header-title">Dashboard</h1>
      </div>
      <div class="header-right">
        <div class="search-container">
    <input type="text" class="search-input" placeholder="Waar ben je naar op zoek?" />
    <i class="fas fa-search search-icon"></i>
  </div>
        <i class="fas fa-cog icon-circle"></i>
        <i class="fas fa-bell icon-circle"></i>
      </div>
    </header>
    <div class="tab-container">
    <div class="tab-item" :class="{ 'active': activeTab === 'overview' }" @click="changeTab('overview')">Mijn Overview</div>
    <div class="tab-item" :class="{ 'active': activeTab === 'finances' }" @click="changeTab('finances')">Financiën</div>
    <div class="tab-item" :class="{ 'active': activeTab === 'sales' }" @click="changeTab('sales')">Sales</div>
    <div class="tab-item" :class="{ 'active': activeTab === 'marketing' }" @click="changeTab('marketing')">Marketing</div>
  </div>
  </template>

<style>
.header {
  display: flex;
  align-items: center;
  justify-content: space-between;
  padding: 10px;
  padding-top: 29px;
}

.tab-container {
  display: flex;
  margin-left: 350px;
  font-family: 'Inter', sans-serif;
  z-index: 1;
}

.tab-item {
  cursor: pointer;
  padding: 10px 30px;
  position: relative;
  z-index: 1;
  color: #A7A7A7;
}

.tab-item.active {
  border-bottom: 3px solid #F37357;
  z-index: 2;
  color: #585858;
}

.icon-circle {
  margin-left: 10px;
  color: #666;
  cursor: pointer;
  border: 1px solid #ccc;
  border-radius: 50%;
  padding: 10px;
}

.search-container {
  display: flex;
  align-items: center;
  border: 1px solid #ccc;
  border-radius: 5px;
  padding: 5px;
}

.search-input {
  flex: 1;
  border: none;
  padding: 5px;
  font-size: 14px;
  margin-right: 200px !important;
}

.search-icon {
  margin-left: 10px;
  color: #666;
  cursor: pointer;
}

.header-left {
  display: flex;
  align-items: center;
}

.header-title {
  margin-left: 350px;
  font-family: 'Inter', sans-serif;
  font-size: 30px;
  color: #192B31;
}

.header-right {
  display: flex;
  align-items: center;
  margin-right: 100px;
}

.search-input {
  margin-right: 10px;
  padding: 5px;
  border: none;
  border-radius: 5px;
}

.fa-cog,
.fa-bell {
  margin-left: 10px;
  cursor: pointer;
}
</style>

<script>
export default {
  data() {
    return {
      activeTab: 'overview'
    };
  },
  methods: {
    changeTab(tab) {
      this.activeTab = tab;
    }
  }
};
</script>