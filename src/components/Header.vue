<template>
    <nav class="header-nav">
      <div class="container">
        <div class="logo">My Portfolio</div>
        <div class="links">
          <router-link class="nav-link" to="/">Home</router-link>
          <router-link class="nav-link" to="/portfolio">Portfolio</router-link>
          <router-link class="nav-link" to="/contact">Contact</router-link>
        </div>
      </div>
    </nav>
  </template>
  
  <script>
  export default {
    name: 'Header'
  }
  </script>
  
  <style scoped>
  .header-nav {
    background-color: palevioletred; /* slate-800 */
    padding: 1rem; /* p-4 */
    color: white; /* text-white */
    box-shadow: 0 4px 6px rgba(0, 0, 0, 0.1); /* shadow-md */
  }
  
  .container {
    max-width: 1200px; /* container */
    margin: 0 auto; /* mx-auto */
    display: flex; /* flex */
    justify-content: space-between; /* justify-between */
    align-items: center; /* items-center */
  }
  
  .logo {
    font-size: 1.125rem; /* text-lg */
    font-weight: bold; /* font-bold */
  }
  
  .links {
    display: flex; /* flex */
    gap: 1rem; /* space-x-4 */
  }
  
  .nav-link {
    color: palevioletred;
    text-decoration: none;
    transition: text-decoration 0.3s;
    background-color: rgb(254, 230, 234);
    padding: 1ch;
    border-radius: 10px;
  }
  
  .nav-link:hover {
    color: thistle;
    background-color: seashell;
  }
  </style>
  