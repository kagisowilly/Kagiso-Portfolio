<template>
  <section
    class="about-section"
    id="about"
  >

<div>     <h1 class="text-center display-6 subtitlee green fw-bold mb-5"><u>About</u></h1></div>
    <div class="container pb-3" >
 
      
                <div class="text-center "><h3  class="text-black mb-4 intro">Introduction</h3></div>
      <div class="row justify-content-center text-black">
        <div class="col col-lg-10 abountcont col-md-10">
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

      <div class="row justify-content-center pt-3">
        <div class="col-lg-6 col-md-5">
          <table class="table text-start  text-black table-bordered">
            <thead>
              <tr>
                <th scope="col">Personal Details</th>
              </tr>
            </thead>
            <tbody>
              <tr>
                <td><b class="text-muted">Full name:</b><span class="green">Kagiso Mphayi</span> </td>
              </tr>
              <tr>
                <td><b class="text-muted">Date of birth:</b> 1996/07/01</td>
              </tr>
              <tr>
                <td><b class="text-muted">Location:</b> Cape Town,South Africa</td>
              </tr>
              <tr>
                <td><b class="text-muted">Cell Phone number:</b> 079 928 2407</td>
              </tr>
            </tbody>
          </table>
        </div>
                <div class="col-lg-6 col-md-5">
          <table class="table text-start text-black table-bordered">
            <thead>
              <tr>
                <th scope="col">Languages</th>
              </tr>
            </thead>
            <tbody>
              <tr>
                <td>English</td>
              </tr>
              <tr>
                <td>Setswana</td>
              </tr>
              <tr>
                <td>Sesotho</td>
              </tr>
              <tr>
                <td>Isizulu</td>
              </tr>
            </tbody>
          </table>
        </div>
        <div class="col col-lg-6 col-md-5">
          <table class="table text-start text-black table-bordered">
            <thead>
              <tr class="text-black">
                <th scope="col text-muted">Passion Board</th>
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

        <div class="col col-lg-6 col-md-5">
          <table class="table text-start text-black table-bordered">
            <thead>
              <tr>
                <th scope="col">Soft Skills</th>
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

      </div>
    </div>

            <div class="container hr">
            <hr class=" bg-white">
        </div>
  </section>
</template>

<script>
export default {};
</script>

<style scoped>
tbody, td, tfoot, th, thead, tr {
    border-color: inherit;
    border-style: solid;
    border-width: 0;
}
.table>:not(:first-child) {
    border-top: 1px solid rgba(115, 179, 106, 0.966);
}
.green{
  color: rgba(115, 179, 106, 0.966);
}


td,tr{
  font-size: large;
}
th{
  font-size: larger;
}
    .abountcont {
      text-align: center;
    }

/* SLIDE */
 section{
  animation-duration: 1s;
  animation-name: slidein;
}
template{
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

</style>

