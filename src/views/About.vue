<template>
  <section class="about-section" id="about">
    <div class="sec">
      <!-- SUBTITLE -->
    <div>
      <h1 class="text-center display-6 subtitlee green fw-bold mb-5">
        <u>ABOUT</u>
      </h1>
    </div>
    <div class="container pb-3">
      <div class="text-center">
        <h5 class="text-black mb-3 intro">INTRODUCTION</h5>
      </div>
      <!-- ABOUT ME PARAGRAPHS -->
      <div class="row justify-content-center text-black">
        <div
          class="
            col col-lg-10
            text-md-start text-lg-center
            text-start
            abount_me
            col-md-10
          "
        >
          <p>
            I am a hard-working individual who never shies away from a
            challenge. I am always willing to help the person next to me.
            Furthermore, I am a good communicator, and this is one of the
            reasons why I work well with people. I am always eager to expand my
            knowledge, and I am a fast learner as well.
          </p>
          <p class="mt-3">
            My passion for the tech industry started from having conversations
            with some of my close friends who are already in the field of
            technology. As someone who is always eager to learn new things and
            who's obsessed with improving the world we live in, my passion
            developed more.
          </p>
        </div>
      </div>
<!-- TABLES -->
      <div class="row justify-content-center pt-3">
        <div class="col- col-lg-6 col-md-5">
          <table class="table text-start text-black table-bordered">
            <thead>
              <tr>
                <th scope="col-">Personal Details</th>
              </tr>
            </thead>
            <tbody>
              <tr>
                <td>
                  <b class="text-muted">Full name:</b>
                  <span class="green">Kagiso Mphayi</span>
                </td>
              </tr>
              <tr>
                <td>
                  <b class="text-muted">Date of birth:</b>
                  1996/07/01
                </td>
              </tr>
              <tr>
                <td>
                  <b class="text-muted">Location:</b>
                  Cape Town,South Africa
                </td>
              </tr>
              <tr>
                <td>
                  <b class="text-muted">Cell Phone number:</b>
                  079 928 2407
                </td>
              </tr>
            </tbody>
          </table>
        </div>

        <div class="col- col-lg-6 col-md-5">
          <table class="table text-start text-black table-bordered">
            <thead>
              <tr class="text-black">
                <th scope="col- text-muted">Passion Board</th>
              </tr>
            </thead>
            <tbody>
              <tr>
                <td>Reading</td>
              </tr>
              <tr>
                <td>Chess</td>
              </tr>
              <tr>
                <td>Mind-Challenging Games</td>
              </tr>
              <tr>
                <td>Online gaming</td>
              </tr>
            </tbody>
          </table>
        </div>

        <div class="col- col-lg-6 col-md-5">
          <table class="table text-start text-black table-bordered">
            <thead>
              <tr>
                <th scope="col-">Soft Skills</th>
              </tr>
            </thead>
            <tbody>
              <tr>
                <td>Communication & Leadership</td>
              </tr>
              <tr>
                <td>Time Management</td>
              </tr>
              <tr>
                <td>Problem-Solving</td>
              </tr>
              <tr>
                <td>Flexibility/Adaptability</td>
              </tr>
            </tbody>
          </table>
        </div>
        <!-- BUTTONS -->
        <div class="col- col-lg-6 col-md-5">
          <div class="hr">
            <hr />
          </div>
          <div class="submit">
            <a
              target="_blank"
              download
              href="https://drive.google.com/u/0/uc?id=1UDy72Sh_qZ-l5TbYVWDQupfgHcpej3Vu&export=download"
              class="text-white"
            >
              <button type="Submit" class="mb-3 btn button-body">
               <span class="download">Download</span>  CV
                <i class="bi bi-download"></i>
              </button>
            </a>
            <a href="">
              <router-link to="/projects">
                <button type="Submit" class="mb-3 buttt btn button-body">
                  My Work
                  <i class="bi mx-1 bi-briefcase"></i>
                </button>
              </router-link>
            </a>
          </div>
        </div>
      </div>
    </div>

    <div class="container hr">
      <hr class="bg-white" />
    </div>      
    </div>

  </section>
</template>

<script>
export default {}
</script>

<style scoped>
/* BACKGROUND */
template {
  background-color: #f2f2fc;
}
/* BUTTON */
.submit{
  display: flex;
  gap: 5px;
}
button:hover {
  opacity: 0.8;
  background: #12613b;
  color: rgb(255, 255, 255) !important;
}
.intro{
  font-weight: bold;
}
.button-body {
  background: rgba(115, 179, 106, 0.966);
  border: 0;
  margin-top: 10px;
  color: black;
  border-radius: 10px;
  cursor: pointer;
}
.buttt {
  margin-left: 10px;
}
/* FONT */
.green {
  color: rgba(115, 179, 106, 0.966);
}
.abount_me {
  text-align: center;
}
/* HORIZONTAL LINE */
hr {
  color: rgba(115, 179, 106, 0.966);
  height: 2px;
  margin-bottom: 0;
  margin-top: 50px;
}
/* TABLES */
tbody,
td,
tfoot,
th,
thead,
tr {
  border-color: inherit;
  border-style: solid;
  border-width: 0;
}
.table > :not(:first-child) {
  border-top: 1px solid rgba(115, 179, 106, 0.966);
}
td,
tr {
  font-size: large;
}
th {
  font-size: larger;
}
/* SLIDE ANIMATION */
.sec {
  animation-duration: 1s;
  animation-name: slidein;
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
/* MEDIA QUERIES */
@media all and (max-width: 991px) {
  .buttt {
    margin-left: 0;
  }
  .button-body {
  background: rgba(115, 179, 106, 0.966);
  border: 0;
  margin-top: 10px;
  color: black;
  border-radius: 10px;
  cursor: pointer;
  font-size: 13px;
  
}
}
@media all and (max-width: 767px) {
  hr {
  margin-top: 15px;
}
  .buttt {
    margin-left: 10px !important;
  }
  tbody,
td,
tfoot,
th,
thead,
tr {
  border-color: inherit;
  border-style: solid;
  border-width: 0;
  padding: 5px;
}
}
@media all and (max-width: 576px) {
  td,
tr {
  font-size: medium;
}
th {
  font-size: large;
}
tbody,
td,
tfoot,
th,
thead,
tr {
  border-color: inherit;
  border-style: solid;
  border-width: 0;
  padding: 2px;
}
}
@media all and (max-width: 461px) {
  .buttt {
    margin-left: 1px !important;
  }
}
@media all and (max-width: 330px) {
  .download{
 display: none; 
}
}

</style>
