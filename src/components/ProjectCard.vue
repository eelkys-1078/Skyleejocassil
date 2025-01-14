<template>
    <div class="bg-white p-4 rounded shadow">
      <img :src="image" alt="Project image" class="project-image">
      <h2 class="text-xl font-semibold">{{ title }}</h2>
      <p class="mt-2">{{ description }}</p>
    </div>
  </template>
  
  <script>
  export default {
    name: 'ProjectCard',
    props: {
      title: {
        type: String,
        required: true
      },
      description: {
        type: String,
        required: true
      },
      image: {
        type: String,
        required: true
      }
    }
  }
  </script>
  
  <style scoped>
  .project-image {
    width: 100%;
    height: auto;
    border-radius: 0.375rem;
    margin-bottom: 1rem;
  }
  </style>
  