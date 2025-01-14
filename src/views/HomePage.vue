<template>
    <div class="container">
      <h1 class="title">Welcome!</h1>
      <p class="description">Hi there! Welcome to my portfolio. I built this site with Vue.js and vanilla CSS to showcase my skills and projects. Please take a look around—I hope you enjoy what you see!</p>
      <img src="/image/visonboard.png" alt="image" class="image">
      <router-link to="/portfolio">
        <button class="btn">My Projects</button>
      </router-link>
    </div>
  </template>
  
  <script>
  export default {
    name: 'HomePage'
  }
  </script>
  
  <style scoped>

   @import url('https://fonts.googleapis.com/css2?family=Poppins:ital,wght@1,100&family=Zen+Loop:ital@0;1&display=swap');
   .container {
  background-image: url('/image/pink.jpeg');
  background-size: cover;
  background-position: center;
  background-repeat: no-repeat;
  font-family: 'Poppins', sans-serif;
  width: 100%;
  height: 100vh;
  display: flex;
  flex-direction: column;
  align-items: center;
  justify-content: center;
  text-align: center;
  padding: 1rem;
}

.title {
  font-family: 'Zen Loop', cursive;
  font-size: 4.25rem; /* Equivalent to text-4xl */
  font-weight: bold;
  color: rgb(112, 12, 46);
}

.description {
  font-size: 1.25rem; /* Equivalent to text-lg */
  color: rgb(112, 12, 46);
  font: bold 1.5rem 'Zen Loop', cursive;
  margin: 1rem 0;
  background-color: rgba(255, 255, 255, 0.5); /* White with 50% opacity */
  border-radius: 1rem;
  padding: 1rem;
}

.image {
  width: 40%;
  height: auto;
  border-radius: 2em;
  box-shadow: 1em 1em 1em rgba(0, 0, 0, 0.1);
  border: 1px solid palevioletred;
  background-color: rgba(255, 255, 255, 0.5); /* White with 50% opacity */
}

.btn {
  flex: auto;
  font-family: 'Poppins', sans-serif;
  font: bold 1.5rem 'Zen Loop', cursive;
  margin-top: 1px;
  padding: 0.5rem 1rem;
  background-color: pink; /* Equivalent to bg-blue-500 */
  color: palevioletred;
  border: 1px solid palevioletred;
  border-radius: 0.375rem;    
  cursor: pointer;
  transition: background-color 0.3s;
  box-shadow: 1em 1em 1em rgba(0, 0, 0, 0.1);
  background-color: rgba(255, 255, 255, 0.5); /* White with 50% opacity */
}

.btn:hover {
  background-color: palevioletred; /* Equivalent to hover:bg-blue-700 */
  color: pink;
}

  </style>
  