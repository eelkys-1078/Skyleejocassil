<template>
    <form class="contact-form">
      <div class="form-group">
        <label class="form-label" for="name">Name</label>
        <input class="form-input" type="text" id="name" />
      </div>
      <div class="form-group">
        <label class="form-label" for="email">Email</label>
        <input class="form-input" type="email" id="email" />
      </div>
      <div class="form-group">
        <label class="form-label" for="message">Message</label>
        <textarea class="form-input" id="message" rows="4"></textarea>
      </div>
      <button class="form-button" type="submit">Send</button>
    </form>
  </template>
  
  <script>
  export default {
    name: 'ContactForm'
  }
  </script>
  
  <style scoped>
  .contact-form {
    margin-top: 1rem;
    background-color: rgba(255, 255, 255, 0.7); /* White with 50% opacity */
    padding: 1rem; /* p-4 */
    border-radius: 0.55rem; /* rounded-sm */  
    margin: 1em;
    font: Poppins 2.5rem; /* font-bold */
    color: black);

  }
  
  .form-group {
    margin-bottom: 1rem;
    margin: 1em;
    font: poppins 1.5rem; /* font-bold */
  }
  
  .form-label {
    display: block;
    font-size: 0.875rem; /* Equivalent to text-sm */
    font-weight: 500; /* Equivalent to font-medium */
    margin-bottom: 0.5rem;
    font: bold 1.5rem 'Zen Loop', cursive;  
    color: palevioletred;
  }
  
  .form-input {
    width: 100%;
    border: 1px solid #ccc; /* Basic border */
    border-radius: 0.25rem; /* Rounded corners */
    padding: 0.5rem; /* Equivalent to p-2 */
    box-sizing: border-box; /* Ensure padding does not affect width */
  }
  
  .form-button {
    background-color: palevioletred;
    color: rgb(250, 216, 222);
    border: none;
    border-radius: 0.25rem; /* Rounded corners */
    padding: 0.5rem 1rem; /* Equivalent to p-2 */
    cursor: pointer;
    transition: background-color 0.3s;
  }
  
  .form-button:hover {
    background-color: rgb(216, 191, 204);
  }
  </style>
  