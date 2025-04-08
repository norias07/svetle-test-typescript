
<script lang="ts">
    let showNavbar = false;
  
    // Function to detect scroll position
    const handleScroll = () => {
      if (window.scrollY > 260) {  // Change this value to control when the navbar appears
        showNavbar = true;
      } else {
        showNavbar = false;
      }
    };
  
    // Set up the scroll event listener
    import { onMount } from 'svelte';
  
    onMount(() => {
      window.addEventListener('scroll', handleScroll);
  
      // Clean up the event listener when the component is destroyed
      return () => {
        window.removeEventListener('scroll', handleScroll);
      };
    });
  </script>
 
 <header>
  <h1>Welcome to Bsides</h1>
  <p>
      This is a test site for Bsides 2025
  </p>
</header>
<div class="navbar {showNavbar ? 'visible' : ''}">
    <nav>
      <!-- Add your navigation items here -->
      <a href="#home">Home</a>
      <a href="#about">About</a>
      <a href="#services">Services</a>
      <a href="#contact">Contact</a>
    </nav>
  </div> 


<style>
  .navbar {
      position: fixed;
      top: 0;
      left: 0;
      right: 0;
      transition: opacity 0.3s;
      background-color: #ba98ff;; 
      background-image: -moz-linear-gradient(90deg, #ba98ff 0%, #8e78ff 100%);
      background-image: -webkit-linear-gradient(90deg, #ba98ff 0%, #8e78ff 100%);
      background-image: -ms-linear-gradient(90deg, #ba98ff 0%, #8e78ff 100%);
      padding: 30px;
      opacity: 0;
      visibility: hidden;
      position: sticky;
      display: flex;
      justify-content: center;
      margin-top: 10px;
     
    }
    .navbar a {
      color: rgb(255, 255, 255);
      text-decoration: none;
      margin: 0 10px;
    }
    .navbar.visible {
      opacity: 1;
      visibility: visible;
    } 
  header {
    background-image: -moz-linear-gradient(90deg, #ba98ff 0%, #8e78ff 100%);
    background-image: -webkit-linear-gradient(90deg, #ba98ff 0%, #8e78ff 100%);
    background-image: -ms-linear-gradient(90deg, #ba98ff 0%, #8e78ff 100%);
    background-color: #ba98ff;
    color: white;
    padding: 1rem;
    text-align: center;
    padding-top: 100px ;
  }
  h1{

      font-size: 3rem;
      
      font-family: "oso-sans-variable",sans-serif;
      font-variation-settings: 'wdth' 100, 'wght' 400;
}
  
</style>

