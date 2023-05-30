<template>
  <nav class="vertical-navbar">
    <div class="user-profile">
  <div class="profile-picture">
    <img src="src/assets/thierry.jpg" alt="">
  </div>
    <div class="user-details">
    <h3 class="user-name">Thierry Schout</h3>
    <p class="user-role">Creative Director</p>
  </div>
  </div>
    <hr class="divider" />
    <ul class="nav-links">
      <li class="nav-link"><i class="icon fas fa-th-large"></i><a href="#">Dashboard</a></li>
      <li class="nav-link"><i class="icon fas fa-credit-card"></i><a href="#">Financiën</a></li>
      <li class="nav-link"><i class="icon fas fa-line-chart"></i><a href="#">Sales</a></li>
      <li class="nav-link"><i class="icon fas fa-users"></i><a href="#">Contacten</a></li>
      <li class="nav-link"><i class="icon fas fa-th-list"></i><a href="#">Projecten</a></li>
      <li class="nav-link"><i class="icon fas fa-bullhorn"></i><a href="#">Marketing</a></li>
      <li class="nav-link"><i class="icon fas fa-calendar"></i><a href="#">Agenda</a></li>
    </ul>
  </nav>
</template>

<style>
.vertical-navbar {
  position: fixed;
  left: 0;
  top: 0;
  height: 100vh;
  width: 293.83px;
  background-color: #F9FAFB;
  border-right: 1px solid #DEE0E5;
}

.avatar {
  width: 40px;
  height: 40px;
  border-radius: 50%;
  margin-right: 10px;
}

.username {
  font-weight: bold;
}

.divider {
  border: none;
  border-top: 1px solid #ccc;
  margin-bottom: 20px;
  width: 100vw;
  z-index: 0;
}

.nav-links {
  list-style: none;
  padding: 0;
  margin: 0;
  margin-top: 50px;
  margin-left: 60px;
}

.user-profile {
  display: flex;
  flex-direction: column;
  align-items: center;
  justify-content: center;
  text-align: center;
  margin-top: 10px;
  margin-bottom: 30px;
  font-family: 'Inter', sans-serif;
}

.nav-link {
  display: flex;
  align-items: center;
  margin-bottom: 30px;
  color: #ABABAB;
  font-size: 20px;
}

.nav-link a {
  text-decoration: none;
  color: #ABABAB;
  margin-left: 10px;
  font-family: 'Inter', sans-serif;
  font-size: 17px;
  margin-left: 30px;
  margin-top: 5px;
}

.icon {
  width: 16px;
  height: 16px;
  margin-right: 5px;
}
</style>

<script>
export default {
  // Componentopties
}
</script>
