<script setup>
defineProps({
    id: String,
    title: String,
    description: String,
    url: String
})

function getImage(title){
    const url = '../assets/images/project'+title+'.jpg'
    return new URL(url, import.meta.url).href
}
function getUrl(title){
    // make a link to github page
}

function viewProject(id){
    return '$route.params.' + id
}

import { RouterView } from 'vue-router';

</script>

<template>
    <div class="project-template">
        <div class="project-image">
            <img :src=getImage(id) alt="None" class="individual-image">
        </div>
        <div class="project-body">
            <div class="project-hover">
            <h1>{{ title }}</h1>
            <p>{{ description }}</p>
            <!-- <a :href=getUrl(title)> {{ url }}</a> -->
        </div>
            <button type="button" class="project-button" @click="viewProject(title)">{{ url }}</button>
        </div>
    </div>
</template>

<style scoped>
 .project-template{
    display: flex;
    font-family: 'Arial', sans-serif;
    background-color: #f4f4f4;
    border-radius: 8px;
    box-shadow: 0 4px 8px rgba(0, 0, 0, 0.1);
    margin-bottom: 3%;

}

.project-image{
   flex: 1;
    border-radius: 3px;
    align-self: center;
    padding-right: 25px;
}

.individual-image {
    max-width: 250px;
    margin: 7%;
    border-radius: 3px;
    margin-left: 10%;
    transition: transform 0.3s, box-shadow 0.3s;
}

.project-image :hover.individual-image {
    transform: scale(1.1);
    box-shadow: 0 4px 15px rgba(0, 0, 0, 0.2);
}


.project-body{
    flex: 2;
    background-color: rgb(212, 212, 212);
    margin: 1%;
    padding: 1% 5%;
    border-radius: 5px;
} 

.project-hover {
    transition: transform 0.3s, padding .3s;
}
.project-body :hover.project-hover  {
    transform: scale(1.05);
    /* padding: 1% 2%; */

}

.project-button {
    background-color: #e74c3c;
    color: #fff;
    padding: 10px 20px;
    border-radius: 5px;
    border: none;
    cursor: pointer;
    transition: background-color 0.3s;
    position: relative;
    left: 38%;
}

.project-button:hover {
  background-color: #c0392b;
} 

@media (max-width: 768px) {
    .project-template {
        flex-direction: column;
    }
    .project-image {
        align-self: center;
    }

}

</style>