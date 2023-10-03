<script setup>
import ProjectsComponent from '../components/ProjectsComponent.vue';
import { ref } from 'vue'

const ProjectsList = ref([
    {id: 1, title: 'Project Title 1', description: 'Project 1 Description Lorem ipsum dolor sit amet, consectetur adipiscing elit, sed do eiusmod tempor incididunt ut labore et dolore magna aliqua. Ut enim ad minim veniam, quis nostrud exercitation ullamco laboris nisi ut aliquip ex ea commodo consequat. Duis aute irure dolor in reprehenderit in voluptate velit esse cillum dolore eu fugiat nulla pariatur', 
      url: 'View on GitHub'},
    {id: 2, title: 'Project Title 2', description: 'Project 2 Description Lorem ipsum dolor sit amet, consectetur adipiscing elit, sed do eiusmod tempor incididunt ut labore et dolore magna aliqua. Ut enim ad minim veniam, quis nostrud exercitation ullamco laboris nisi ut aliquip ex ea commodo consequat. Duis aute irure dolor in reprehenderit in voluptate velit esse cillum dolore eu fugiat nulla pariatur', 
      url: 'View on GitHub'},
    {id: 3, title: 'Project Title 3', description: 'Project 3 Description Lorem ipsum dolor sit amet, consectetur adipiscing elit, sed do eiusmod tempor incididunt ut labore et dolore magna aliqua. Ut enim ad minim veniam, quis nostrud exercitation ullamco laboris nisi ut aliquip ex ea commodo consequat. Duis aute irure dolor in reprehenderit in voluptate velit esse cillum dolore eu fugiat nulla pariatur', 
      url: 'View on GitHub'},
    {id: 4, title: 'Project Title 4', description: 'Project 4 Description Lorem ipsum dolor sit amet, consectetur adipiscing elit, sed do eiusmod tempor incididunt ut labore et dolore magna aliqua. Ut enim ad minim veniam, quis nostrud exercitation ullamco laboris nisi ut aliquip ex ea commodo consequat. Duis aute irure dolor in reprehenderit in voluptate velit esse cillum dolore eu fugiat nulla pariatur', 
      url: 'View on GitHub'},
    {id: 5, title: 'Project Title 5', description: 'Project 5 Description Lorem ipsum dolor sit amet, consectetur adipiscing elit, sed do eiusmod tempor incididunt ut labore et dolore magna aliqua. Ut enim ad minim veniam, quis nostrud exercitation ullamco laboris nisi ut aliquip ex ea commodo consequat. Duis aute irure dolor in reprehenderit in voluptate velit esse cillum dolore eu fugiat nulla pariatur', 
      url: 'View on GitHub'},    
])


</script>

<template>
    <div class="main-template">
      <div class="main-section">
        <h1>My Projects</h1>
        <p>Feel free to browse through some of my past and current projects</p>
      
    <div class="project-component" v-for="project in ProjectsList" :key="title">
        <ProjectsComponent v-bind="project"/>
        
    </div>
  </div>
  </div>
        
    
</template>

<style scoped>

.main-template{
  flex-direction: column;
}

h1 {
  align-self: center;
}

</style>