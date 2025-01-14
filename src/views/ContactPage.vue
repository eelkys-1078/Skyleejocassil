<template>
    <div class="container mx-auto p-4">
      <h1 class="text-4xl font-bold">Contact Me</h1>
      <ContactForm />
    </div>
  </template>
  
  <script>
  import ContactForm from '../components/ContactForm.vue';
  
  export default {
    name: 'ContactPage',
    components: {
      ContactForm
    }
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
  font: bolder .5rem 'Zen Loop', cursive;
    }
    h1 {
        margin-bottom: 1rem;
        font-family: 'Zen Loop', cursive;
        font-size: 4.25rem; /* Equivalent to text-4xl */
        font-weight: bold;  
        text-align: center;
    }   
  </style>
  