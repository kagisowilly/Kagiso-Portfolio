<template>
    <h1 class="text-center display-6 subtitlee fw-bold"><u>Skills</u></h1>
  <section id="skills" style="">
    <div class="container skills-content col-lg-6 col-md-8 col-sm-10 col-10 mt-5">
      <div class="text-white">
        <label class="text-black">HTML</label>
        <div class="bar d-flex">
          <div class="rating slide text-center" style="height: 24px; width: 80%">
           <p>70-90%</p> 
          </div>         
        </div>
        <br />
      <label class="text-black">CSS</label>
        <div class="bar d-flex">
          <div class="rating slide" style="height: 24px; width: 75%">
           <p>70-90% </p> 
          </div>
          
        </div>
        <br />
      <label class="text-black">JavaScript</label>
        <div class="bar d-flex">
          <div class="rating slide" style="height: 24px; width: 65%">
            <p>50-75%</p>
          </div>
        </div>
        <br />
       <label class="text-black">Vue JS</label>
        <div class="bar d-flex">
          <div class="rating slide" style="height: 24px; width: 80%">
            <p>75-95%</p>
          </div> 
        </div>
        <br />
        <label class="text-black">MySQL</label>
        <div class="bar d-flex">
          <div class="rating slide" style="height: 24px; width: 90%">
           <p>80-100%</p>
          </div> 
        </div>
        <br />
      <label class="text-black">Node JS</label>
        <div class="bar d-flex">
          <div class="rating slide" style="height: 24px; width: 65%">
            <p>50-75%</p>
          </div>
        </div>
        <br />
        <label class="text-black">PostgreSQL</label>
        <div class="bar d-flex">
          <div class="rating slide" style="height: 24px; width: 75%">
            <p>75-90%</p>
          </div>
        </div>
        <br />
        <label class="text-black">MongoDB</label>
        <div class="bar d-flex">
          <div class="rating slide" style="height: 24px; width: 73%">
            <p>70-80%</p>
          </div>
        </div>
        <br />
      </div>
    </div>
  </section>
</template>

<script>
export default {}
</script>

<style scoped>
.subtitlee{
   color: rgba(115, 179, 106, 0.966);
}
#skills{
  height: 92vh;
  display: flex;
  justify-content: center;
  align-items: center;
}
p{
  position:absolute;
  left:50%;
}
.rating {
  background-color: rgba(115, 179, 106, 0.966);
}
.bar {
  background-color: rgb(223, 223, 223);
}
/* SLIDE */
.slide {
  animation-duration: 3s;
  animation-name: slidein;
}
template {
  background-color: #f2f2fc;
}
@keyframes slidein {
  from {
    margin-left: 0%;
    width: 0%;
  }
  to {
    margin-right: 0%;
    max-width: 100%;
  }
}
/* SLIDE END */
</style>
