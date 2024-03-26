<template>
   <div class="snip1568" id="" style="width: 18rem;" v-for="Testimonials in testimonial " :key="Testimonials">
  <figcaption>
    <h3 class="card-title mt-2">{{Testimonials.name}}</h3>
    <h4 class="card-subtitle">{{ Testimonials.surname }}</h4>
    <span class="card-text">{{Testimonials.quotes}}</span>

  </figcaption>
  <img class="card-images" :src=" Testimonials.profile" loading="lazy" alt="Profile picture" width="200" height="200">
    <div class="icons"><a href="#"><i class="ion-social-reddit"></i></a>
      <a href="#"> <i class="ion-social-twitter"></i></a>
      <a href="#"> <i class="ion-social-vimeo"></i></a>
    </div>
  </div>
<!-- </div> -->
<!-- <div class="snip1568">
  <figcaption>
    <h3>Will Barrow</h3>
    <h4>Web Designer</h4>
    <p>I'm killing time while I wait for life to shower me with meaning and happiness.</p>
  </figcaption>
  <div class="profile-image"><img src="https://s3-us-west-2.amazonaws.com/s.cdpn.io/331810/profile-sample7.jpg" alt="profile-sample7" />
    <div class="icons"><a href="#"><i class="ion-social-reddit"></i></a>
      <a href="#"> <i class="ion-social-twitter"></i></a>
      <a href="#"> <i class="ion-social-vimeo"></i></a>
    </div>
  </div>
</div>
<div class="snip1568">
  <figcaption>
    <h3>Indigo Violet</h3>
    <h4>Public Relations</h4>
    <p>The only skills I have the patience to learn are those that have no real application in life. </p>
  </figcaption>
  <div class="profile-image"><img src="https://s3-us-west-2.amazonaws.com/s.cdpn.io/331810/profile-sample6.jpg" alt="profile-sample6" />
    <div class="icons"><a href="#"><i class="ion-social-reddit"></i></a>
      <a href="#"> <i class="ion-social-twitter"></i></a>
      <a href="#"> <i class="ion-social-vimeo"></i></a>
    </div>
  </div>
</div> -->
</template>
<script>

export default {
    computed:{
        testimonial(){
            return this.$store.state.testimonials;
        }
    },
    mounted(){
        this.$store.dispatch("fetchTestimonials")
    }
    
}
</script>
<style >
body{
    background-image: radial-gradient(circle at center center, transparent 0%,rgb(0,0,0) 85%),linear-gradient(78deg, rgba(192, 192, 192,0.05) 0%, rgba(192, 192, 192,0.05) 50%,rgba(60, 60, 60,0.05) 50%, rgba(60, 60, 60,0.05) 100%),linear-gradient(227deg, rgba(97, 97, 97,0.05) 0%, rgba(97, 97, 97,0.05) 50%,rgba(52, 52, 52,0.05) 50%, rgba(52, 52, 52,0.05) 100%),linear-gradient(240deg, rgba(98, 98, 98,0.05) 0%, rgba(98, 98, 98,0.05) 50%,rgba(249, 249, 249,0.05) 50%, rgba(249, 249, 249,0.05) 100%),linear-gradient(187deg, rgba(1, 1, 1,0.05) 0%, rgba(1, 1, 1,0.05) 50%,rgba(202, 202, 202,0.05) 50%, rgba(202, 202, 202,0.05) 100%),linear-gradient(101deg, rgba(61, 61, 61,0.05) 0%, rgba(61, 61, 61,0.05) 50%,rgba(254, 254, 254,0.05) 50%, rgba(254, 254, 254,0.05) 100%),linear-gradient(176deg, rgba(237, 237, 237,0.05) 0%, rgba(237, 237, 237,0.05) 50%,rgba(147, 147, 147,0.05) 50%, rgba(147, 147, 147,0.05) 100%),linear-gradient(304deg, rgba(183, 183, 183,0.05) 0%, rgba(183, 183, 183,0.05) 50%,rgba(57, 57, 57,0.05) 50%, rgba(57, 57, 57,0.05) 100%),radial-gradient(circle at center center, hsl(351,4%,12%),hsl(351,4%,12%));
}
.card{
    background-color: black;
    color: white;
  border: 1px solid #ccc;
  border-radius: 8px;
  padding: 16px;
  margin-left: 16px;
  /* Add any other styling as needed */
}
@import url(https://fonts.googleapis.com/css?family=Montserrat);
@import url(https://code.ionicframework.com/ionicons/2.0.1/css/ionicons.min.css);
@import url(https://fonts.googleapis.com/css?family=Open+Sans);
.snip1568 {
  font-family: 'Open Sans', Arial, sans-serif;
  position: relative;
  display: inline-block;
  margin: 10px;
  min-width: 230px;
  max-width: 315px;
  width: 100%;
  color: #141414;
  text-align: left;
  line-height: 1.4em;
  font-size: 14px;
  box-shadow: none !important;
}

.snip1568 * {
  -webkit-box-sizing: border-box;
  box-sizing: border-box;
}

.snip1568 .profile-image img {
  border-radius: 5px;
  max-width: 100%;
  height: 80px;
  vertical-align: top;
  float: left;
}

.snip1568 figcaption {
  width: 100%;
  background-color: #333333;
  color: #fff;
  padding: 25px;
  display: inline-block;
  margin-bottom: 15px;
  border-radius: 5px;
  position: relative;
}

.snip1568 figcaption:after {
  content: '';
  position: absolute;
  left: 32px;
  top: 100%;
  width: 0;
  height: 0;
  border-style: solid;
  border-width: 10px 10px 0 10px;
  border-color: #333333 transparent transparent transparent;
}

.snip1568 h3,
.snip1568 h4,
.snip1568 p {
  margin: 0 0 5px;
}

.snip1568 h3 {
  font-weight: 600;
  font-size: 1.2em;
  font-family: 'Montserrat', Arial, sans-serif;
}

.snip1568 h4 {
  color: #8c8c8c;
  font-weight: 400;
  letter-spacing: 2px;
}

.snip1568 p {
  font-size: 0.9em;
  letter-spacing: 1px;
  opacity: 0.9;
}

.snip1568 .icons {
  padding: 20px 90px;
}

.snip1568 i {
  padding: 10px 2px;
  display: inline-block;
  font-size: 18px;
  font-weight: normal;
  color: #ffffff;
  opacity: 0.75;
}

.snip1568 i:hover {
  opacity: 1;
  -webkit-transition: all 0.35s ease;
  transition: all 0.35s ease;
}

/* Demo purposes only */
body {
  background-color: #212121;
}

    
</style>