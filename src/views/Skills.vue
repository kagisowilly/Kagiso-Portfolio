<template>
  <h1 class="text-center display-6 subtitlee fw-bold"><u>Skills</u></h1>
  <section id="skills" style="">
    <div
      class="container skills-content col-lg-6 col-md-8 col-sm-10 col-10 mt-5"
    >
      <div class="text-black">
        <div>
          <div class="labell">
            <label class="text-black"><b>HTML</b></label>
            <p>85%</p>
          </div>
          <div class="bar d-flex">
            <div
              class="rating slide text-center"
              style="height: 24px; width: 85%"
            ></div>
          </div>
        </div>
        <div>
          <div class="labell">
            <label class="text-black"><b>CSS</b></label>
            <p>80%</p>
          </div>
          <div class="bar d-flex">
            <div
              class="rating slide text-center"
              style="height: 24px; width: 80%"
            ></div>
          </div>
        </div>
        <div>
          <div class="labell">
            <label class="text-black"><b>JavaScript</b></label>
            <p>70%</p>
          </div>
          <div class="bar d-flex">
            <div
              class="rating slide text-center"
              style="height: 24px; width: 70%"
            ></div>
          </div>
        </div>
        <div>
          <div class="labell">
            <label class="text-black"><b>Vue.JS</b></label>
            <p>80%</p>
          </div>
          <div class="bar d-flex">
            <div
              class="rating slide text-center"
              style="height: 24px; width: 80%"
            ></div>
          </div>
        </div>
        <div>
          <div class="labell">
            <label class="text-black"><b>Node.JS</b></label>
            <p>78%</p>
          </div>
          <div class="bar d-flex">
            <div
              class="rating slide text-center"
              style="height: 24px; width: 78%"
            ></div>
          </div>
        </div>
        <div>
          <div class="labell">
            <label class="text-black"><b>MongoDB</b></label>
            <p>73%</p>
          </div>
          <div class="bar d-flex">
            <div
              class="rating slide text-center"
              style="height: 24px; width: 73%"
            ></div>
          </div>
        </div>
        <div>
          <div class="labell">
            <label class="text-black"><b>MySQL</b></label>
            <p>87%</p>
          </div>
          <div class="bar d-flex">
            <div
              class="rating slide text-center"
              style="height: 24px; width: 87%"
            ></div>
          </div>
        </div>
        <div>
          <div class="labell">
            <label class="text-black"><b>PostgreSQL</b></label>
            <p>83%</p>
          </div>
          <div class="bar d-flex">
            <div
              class="rating slide text-center"
              style="height: 24px; width: 83%"
            ></div>
          </div>
        </div>
      </div>
    </div>
  </section>
</template>

<script>
export default {}
</script>

<style scoped>
.labell {
  display: flex;
  justify-content: space-between;
  margin-top: 12px;
}
.subtitlee {
  color: rgba(115, 179, 106, 0.966);
}
#skills {
  height: 92vh;
  display: flex;
  justify-content: center;
  align-items: center;
}
p{
margin-bottom: 0;
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
