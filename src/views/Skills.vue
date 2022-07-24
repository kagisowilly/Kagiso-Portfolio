<template>
  <h1 class="text-center display-6 subtitlee fw-bold"><u>SKILLS</u></h1>
  <section id="skill" >
    <p class="container text-muted text-center">Check ourt some  some of the skills I've acquired thus far.</p>
    <div class="skills-page slide">
    <div
      class="container  skills-content mt-5"
    >
    <div class="row skills-div  text-center">
      <div class="icon-div col-lg-2 col-md-3 col-sm-3 col-3"><i class="devicon devicon-html5-plain-wordmark"></i></div>
      <div class="icon-div col-lg-2 col-md-3 col-sm-3 col-3"><i class="devicon devicon-css3-plain-wordmark"></i></div>
      <div class="icon-div col-lg-2 col-md-3 col-sm-3 col-3"><i class="devicon devicon-javascript-plain"></i></div>
      <div class="icon-div col-lg-2 col-md-3 col-sm-3 col-3"><i class="devicon devicon-bootstrap-plain-wordmark"></i></div>
      <div class="icon-div col-lg-2 col-md-3 col-sm-3 col-3"><i class="devicon devicon-vuejs-plain-wordmark"></i></div>
      <div class="icon-div col-lg-2 col-md-3 col-sm-3 col-3"><i class="devicon devicon-nodejs-plain"></i></div>
      <div class="icon-div col-lg-2 col-md-3 col-sm-3 col-3"><i class="devicon devicon-mysql-plain"></i></div>
      <div class="icon-div col-lg-2 col-md-3 col-sm-3 col-3"><i class="devicon devicon-postgresql-plain-wordmark"></i></div>
      <div class="icon-div col-lg-2 col-md-3 col-sm-3 col-3"><i class="devicon devicon-mongodb-plain-wordmark"></i></div>

    </div>

    </div>
    </div>

  </section>
</template>

<script>
export default {}
</script>

<style scoped>
.skills-content{
  display: flex;
justify-content: center ;
}
.icon-div{
padding: 0 !important;
}
.skills-div{
  gap: 100px;
  width: 75%;
  justify-content: center;
}
.skills-page{
  min-height: 85vh;
  align-items: center;
  display: flex;
}
.devicon{
   font-size: 130px; 
   color:rgba(115, 179, 106, 0.966) ;
}
.labell {
  display: flex;
  justify-content: space-between;
  margin-top: 12px;
}

#skills {
  min-height: 100vh;
  display: flex;
  justify-content: center;
}
/* SLIDE */
.slide {
  animation-duration: 1s;
  animation-name: slidein;
}
template {
  background-color: #f2f2fc;
}
@keyframes slidein {
  from {
    margin-left: 100%;
    width: 100%;
  }

  to {
    margin-left: 0%;
    width: 100%;
  }
}
/* SLIDE END */

/* RESPONSIVENESS */
@media all and (max-width: 1400px) {
  .skills-div{
  gap: 100px;
  width: 90%;
}
}
@media all and (max-width: 1200px) {
  .skills-div{
  gap: 100px;
  width: 100%;
}
}
@media all and (max-width: 992px) {
  .skills-div{
  gap: 50px;
  width: 100%;
}
}
@media all and (max-width: 767px) {
.skills-div{
  gap: 50px;
}
.devicon{
   font-size: 80px; 
}
}
@media all and (max-width: 576px) {
.devicon{
   font-size: 70px; 
}
.skills-div{
  gap: 30px 50px;
}
.skills-page{
  min-height: 60vh;
}
}
@media all and (max-width: 450px) {

}
</style>
