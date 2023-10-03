<script setup>
</script>

<template>
  <div class="main-template">
    <div class="main-section">
    <h1>Hello and welcome to my resume website</h1>
    <p> Feel free to explore the site for indepth explanations of my previous projects, 
      currekt skillsets, desired skills and opportunities, or just read the tldr to the right</p>
    
    <p>If you are browsing my resume and would like to send me a job request, please fill out the 
      contact form and I will get back to you.
    </p>
    <p>Thanks for visiting!</p>
    </div>

    <div class="right-section">
      <div class="hover-effect">
      <h3>TLDR on the rest of the site</h3>
      <p>This is just some Filler for a tldr
        <ul> 
          <li>My Name</li>
          <li>My Age</li>
          <li>Current Job Role</li>
          <li>One Pers Quality</li>
          <li>Two Pers Quality</li>
          <li>Three Pers Quality</li>
          <li>Four Pers Quality</li>
          <li>Not Highly Motivated</li>
        </ul>
      </p>
    </div>
    </div>
  </div>

</template>

<style scoped>


.right-section{
  flex:.3;
  padding: 0% 5%;
  color: rgb(55, 55, 55);
  border-radius: 3%;
  margin-left: 1%;
  padding-top: 1%;
  margin-bottom: 3%;
}

div.hover-effect {
  border-radius: 3px;
  transition: transform 0.3s; 
  
}
 
.right-section div:hover {
  transform: scale(1.2);
}

p{
  padding: 1%;
}

ul{
  list-style-type: square;
}

@media (max-width: 768px) {

  .right-section{
    width: 90%;
  }
  div.hover-effect {
  border-radius: 3px;
  transition: transform 0.3s, box-shadow 0.3s;
  padding-left: 20%;
  margin: 2% 6%;
}
 
.right-section div:hover {
  transform: scale(1.1);
  box-shadow: 10px 4px 15px rgba(0, 0, 0, 0.2);
}
}
</style> 