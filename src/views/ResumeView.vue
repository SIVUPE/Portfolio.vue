<template lang="">
    <div>
        <h1 class="display-5">resume</h1>
        <div class="container vh-150">
       <h5 >Education</h5>
      <div class="row mx-5">
           <div class="card m-5 " id="" style="width: 18rem;" v-for="Education in education " :key="Education">
     <div class="card-body">
       <img class="card-images" :src=" Education.picture" loading="lazy" alt="Profile picture" width="150" height="150">
       <h3 class="card-title">{{Education.year}}</h3>
       <h4 class="card-subtitle">{{ Education.description }}</h4>
       <h4 class="card-subtitle">{{ Education.place }}</h4>
     </div>
        </div>

      </div>
    </div>    
    </div>
    <div class="container vh-150">
       <h5 >Skills</h5>
      <div class="row mx-5">
           <div class="card m-5 " id="" style="width: 12rem;" v-for="Skills in skills " :key="Skills">
     <div class="card-body">
       <img class="card-images" :src=" Skills.item" loading="lazy" alt="Profile picture" width="150" height="150">
       <h3 class="card-title">{{Skills.name}}</h3>
       <h4 class="card-subtitle">{{ Skills.surname }}</h4>
     </div>
   </div>
   
      </div>
   </div>
</template>
<script>
export default {
    computed: {
        education() {
            return this.$store.state.education;
        },
        skills() {
            return this.$store.state.skills;
        }
    },
    mounted() {
        this.$store.dispatch("fetchEducation")
        this.$store.dispatch("fetchSkills")
    }

}
</script>
<style>
body{
  background-image: radial-gradient(circle at center center, transparent 0%,rgb(0,0,0) 85%),linear-gradient(78deg, rgba(192, 192, 192,0.05) 0%, rgba(192, 192, 192,0.05) 50%,rgba(60, 60, 60,0.05) 50%, rgba(60, 60, 60,0.05) 100%),linear-gradient(227deg, rgba(97, 97, 97,0.05) 0%, rgba(97, 97, 97,0.05) 50%,rgba(52, 52, 52,0.05) 50%, rgba(52, 52, 52,0.05) 100%),linear-gradient(240deg, rgba(98, 98, 98,0.05) 0%, rgba(98, 98, 98,0.05) 50%,rgba(249, 249, 249,0.05) 50%, rgba(249, 249, 249,0.05) 100%),linear-gradient(187deg, rgba(1, 1, 1,0.05) 0%, rgba(1, 1, 1,0.05) 50%,rgba(202, 202, 202,0.05) 50%, rgba(202, 202, 202,0.05) 100%),linear-gradient(101deg, rgba(61, 61, 61,0.05) 0%, rgba(61, 61, 61,0.05) 50%,rgba(254, 254, 254,0.05) 50%, rgba(254, 254, 254,0.05) 100%),linear-gradient(176deg, rgba(237, 237, 237,0.05) 0%, rgba(237, 237, 237,0.05) 50%,rgba(147, 147, 147,0.05) 50%, rgba(147, 147, 147,0.05) 100%),linear-gradient(304deg, rgba(183, 183, 183,0.05) 0%, rgba(183, 183, 183,0.05) 50%,rgba(57, 57, 57,0.05) 50%, rgba(57, 57, 57,0.05) 100%),radial-gradient(circle at center center, hsl(351,4%,12%),hsl(351,4%,12%));
}
.card{
  background-color: black;
}
</style>