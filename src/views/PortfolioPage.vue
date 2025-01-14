<template>
    <div class="container mx-auto p-4">
      <h1 class="title">My Projects</h1>
      <div class="project-groups">
        <div v-for="group in projectGroups" :key="group.name" class="project-group">
          <div class="button-container">
            <button @click="toggleGroup(group.name)" class="group-button">
              {{ group.name }}
            </button>
          </div>
          <div v-show="group.isOpen" class="projects-list">
            <ProjectCard
              v-for="(project, index) in group.projects"
              :key="index"
              :title="project.title"
              :description="project.description"
              :image="project.image"
            />
          </div>
        </div>
      </div>
    </div>
  </template>
  
  <script>
  import ProjectCard from '../components/ProjectCard.vue';
  
  export default {
    name: 'PortfolioPage',
    components: {
      ProjectCard
    },
    data() {
      return {
        projectGroups: [
          {
            name: 'UI Design',
            isOpen: false,
            projects: [
              { title: 'UI Project 1', description: 'Description for UI Project 1', image: '/images/ui1.png' },
              { title: 'UI Project 2', description: 'Description for UI Project 2', image: '/images/ui2.png' }
            ]
          },
          {
            name: 'UX',
            isOpen: false,
            projects: [
              { title: 'UX Project 1', description: 'Description for UX Project 1', image: '/images/ux1.png' },
              { title: 'UX Project 2', description: 'Description for UX Project 2', image: '/images/ux2.png' }
            ]
          },
          {
            name: 'Development',
            isOpen: false,
            projects: [
              { title: 'Dev Project 1', description: 'Description for Dev Project 1', image: '/images/dev1.png' },
              { title: 'Dev Project 2', description: 'Description for Dev Project 2', image: '/images/dev2.png' }
            ]
          }
        ]
      };
    },
    methods: {
      toggleGroup(groupName) {
        const group = this.projectGroups.find(g => g.name === groupName);
        group.isOpen = !group.isOpen;
      }
    }
  }
  </script>
  
  <style scoped>
  @import url('https://fonts.googleapis.com/css2?family=Poppins:ital,wght@1,100&family=Zen+Loop:ital@0;1&display=swap');
  .title {
    font-family: 'Zen Loop', cursive;
    font-size: 4.25rem; /* Equivalent to text-4xl */
    font-weight: bold;
    color: rgb(112, 12, 46);
  } 
  .container {
    background-image: url('/image/pink.jpeg');
    background-size: cover;
    background-position: center;
    background-repeat: no-repeat;
    font-family: 'Poppins', sans-serif;
    width: 100%;
    min-height: 100vh; /* Ensure the container covers the full viewport height */
    display: flex;
    flex-direction: column;
    align-items: center;
    text-align: center;
    padding: 1rem;
    margin: 0 auto; /* Center the container */
  }
  
  .project-groups {
    margin-top: 2rem;
    width: 100%;
    background-color: rgba(255, 255, 255, 0.5); /* White with 50% opacity */
    padding: 1rem;
    padding-top: 2em;
    border-radius: 0.375rem;
  }
  
  .project-group {
    margin-bottom: 1rem;
  }
  
  .button-container {
    display: flex;
    justify-content: center;
    align-items: center;
  }
  
  .group-button {
    display: block;
    width: 75%;
    padding: 0.5rem;
    background-color: pink; /* Blue color */
    color: darkpink; /* White text color */
    font: bold 1.125rem 'Zen Loop', cursive;
    text-align: center; /* Center the text inside the button */
    border: none;
    border-radius: 0.375rem; /* Rounded corners */
    cursor: pointer;
    transition: background-color 0.3s;
    font-family: 'Zen Loop', cursive;
  }
  
  .group-button:hover {
    background-color: palevioletred;
  }
  
  .projects-list {
    margin-top: 1rem;
    text-align: center;
  }
  </style>
  