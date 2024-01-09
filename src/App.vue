<template>
  <!-- <nav>
    <router-link to="/">Home</router-link> |
    <router-link to="/about">About</router-link> |
    <router-link to="/resume">Resume</router-link> |
    <router-link to="/testimonials">Testimonials</router-link> |
    <router-link to="/skills">Skills</router-link> |
    <router-link to="/contact">Contact</router-link>
  </nav> -->
  <navbar>
    
      <main class="container-fluid">
        <router-view/>
     </main>  
  </navbar>
  <Footer>
  </Footer>
  
</template>
<script>
import Navbar from './components/Navbar.vue';
import Footer from './components/Footer.vue';

export default {
  components:{
    Navbar,
    Footer
  }
}
</script>
<style src="@/assets/css/style.css">
</style>
