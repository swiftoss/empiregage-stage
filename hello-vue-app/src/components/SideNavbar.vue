<template>
    <nav class="navbar">
      <ul class="nav-links">
        <li class="nav-link"><a href="#">Home</a></li>
        <li class="nav-link"><a href="#">Over ons</a></li>
        <li class="nav-link"><a href="#">Diensten</a></li>
        <li class="nav-link"><a href="#">Producten</a></li>
        <li class="nav-link"><a href="#">Blog</a></li>
        <li class="nav-link"><a href="#">Contact</a></li>
      </ul>
    </nav>
  </template>
  
  <style>
  .navbar {
    position: fixed;
    left: 0;
    top: 0;
    height: 100vh;
    width: 200px;
    background-color: #f0f0f0;
    padding: 20px;
  }
  
  .nav-links {
    list-style: none;
    padding: 0;
    margin: 0;
  }
  
  .nav-link {
    margin-bottom: 10px;
  }
  
  .nav-link a {
    text-decoration: none;
    color: #333;
  }
  
  .nav-link a:hover {
    color: #000;
  }
  </style>