<template>

  <div>
  
    <Navbar />
      
        <main class="container-fluid">
          <router-view/>
       </main>  
   
    <Footer />
    <Spinner />

</div>
  
</template>
<script>
import Navbar from './components/Navbar.vue';
import Footer from './components/Footer.vue';
import Spinner from './components/Spinner.vue';

export default {
  components:{
    Navbar,
    Footer,
    Spinner
  }
}
</script>
<style src="@/assets/css/style.css">
</style>
