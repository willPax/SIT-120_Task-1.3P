<template>
    <div class="nav-container">
        <input type="checkbox" id="menu-toggle" class="menu-toggle" />
        <label for="menu-toggle" class="dropdown-btn">Menu</label>
        <div class="links-container" type="checkbox">
            <RouterLink class="nav-link" to="/">Home</RouterLink>
            <RouterLink class="nav-link" to="/about">About</RouterLink>
            <RouterLink class="nav-link" to="/experience">Experience</RouterLink>
            <RouterLink class="nav-link" to="/projects">Projects</RouterLink>
            <RouterLink class="nav-link" to="/contact">Contact </RouterLink>
        </div>
    </div>
</template>

<style scoped>

.nav-container {
  display: flex;
  justify-content: center;
  background-color: #2B3339;
  padding: 10px 0;
  position: relative;
  flex-wrap: wrap;
  
}
 
.nav-link {
  text-decoration: none;
  color: #ecf0f1;
  padding: 10px 20px;
  margin: 0 10px;
  font-size: 1.1em;
  transition: background-color 0.3s, color 0.3s;
  border-radius: 4px;
}
 
.nav-link:hover {
  background-color: #34495e;
  color: #bdc3c7;
}
 
.router-link-active {
  color: #ecf0f1;
  background-color: #c0392b;
  border-radius: 4px;
}
.router-link-active:hover {
  background-color: #9c2f22;
  color: #bdc3c7;
}
 
/* Mobile styles */
.menu-toggle {
  display: none; /* hide the checkbox */
}
 
.dropdown-btn {
  display: none;
  background-color: #34495e;
  color: #ecf0f1;
  padding: 10px 20px;
  border: none;
  cursor: pointer;
  border-radius: 4px;
}
 
.links-container {
  display: flex;
}
 
/* Media query for small screens */
@media (max-width: 768px) {

    .nav-container{
        justify-content: right;
    }
  .dropdown-btn {
    display: block;
    padding: 2% 8%;
    margin-right: 4%; /* easier for mobile users? */
  }
 
  .links-container {
    display: none;
    flex-direction: column;
    position: absolute;
    top: 100%;
    left: 0;
    right: 0;
    background-color: #2c3e50;
    padding-bottom: 1%;
  }
  
 
  .menu-toggle:checked + .dropdown-btn + .links-container {
    display: flex; 
  }

  

}

</style>