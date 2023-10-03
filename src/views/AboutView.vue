<template>
  <section class="main-template">
    <div class="profile-image">
      <img src="../assets/images/sunsetCup.png" alt="Your Name" class="hover-effect">
    </div>
    <div class="main-section">
      <h1>About Me</h1>
      <p>
        Hello! I'm Person, a passionate web developer with over 0 years of experience in creating dynamic and responsive websites. I specialize in specific technologies and fields, e.g., React, Vue.js, and Node.js.
      </p>
      <p>
        I graduated from  University or School with a degree. Since then, I've worked with various clients and companies, delivering high-quality web solutions.
      </p>
      <p>
        In my free time, I love hobbies, e.g., hiking, reading tech blogs, and exploring new coffee shops.
      </p>
      <button class="download-btn">Download My Resume</button>
      <p>
        Thank you for visiting my portfolio. If you'd like to collaborate or just chat, feel free to <a href="mailto:your-email@example.com">reach out</a>!
      </p>
    </div>
  </section>
</template>
 
 
<style scoped>

.profile-image {
  flex: .3;
  padding: 0% 1% 0% 1%;
}
 
.profile-image img.hover-effect {
  /* max-width: 100%; */
  border-radius: 3%;
  transition: transform 0.3s, box-shadow 0.3s;
}
 
.profile-image img.hover-effect:hover {
  transform: scale(1.05);
  box-shadow: 0 4px 15px rgba(0, 0, 0, 0.2);
}
 
 
.main-section h1 {
  font-size: 2.5em;
  margin-bottom: 20px;
}
 
.main-section p {
  margin-bottom: 20px;
  line-height: 1.6;
}
 
.main-section a {
  color: #e74c3c;
  text-decoration: none;
  transition: color 0.3s;
}
 
.main-section a:hover {
  color: #c0392b;
}
 
.download-btn {
  display: inline-block;
  background-color: #e74c3c;
  color: #fff;
  padding: 10px 20px;
  border-radius: 5px;
  border: none;
  cursor: pointer;
  transition: background-color 0.3s;
}
 
.download-btn:hover {
  background-color: #c0392b;
} 

@media (max-width: 800px) {
.profile-image{
  max-width: 40%;
  max-height: 40%;
  align-self: center;
  padding: 0.5% 0%;
}
.profile-image img.hover-effect {
  max-width: 100%;
  max-height: 100%;
}

  

}
</style>