<script setup>
import { RouterLink, RouterView } from 'vue-router'
import NavigationBar from './components/NavigationBar.vue';
import FooterComponent from './components/FooterComponent.vue';
</script>
 
<template>
 <NavigationBar/>
  <div class="page-container">
    <div class="content-wrapper">
      <RouterView />
    </div>

      <FooterComponent />
  </div>

</template>
 
<style scoped>
</style>