<template>
  <!-- RESUME -->

  <section
    class="education-work"
    id="education"
  >
            <h1 class="text-center display-6 green fw-bold subtitlee mb-5">
            <u>Resume</u>
          </h1>
          <h3 class="text-center pt-5">Education & Experience</h3>
    <div class="container mb-5">
      <div class="row  justify-content-center" v-if="resumes">
        <div class="col-lg-10 text-black">

          <ul class="timeline">
            <li class="slide" v-for="resume of resumes" :key="resume.title">
              <div class="resu box-shadow">
                <div class="p-2">
                  <h3 class="green">
                    <i class="bi bi-briefcase-fill"></i> {{resume.title}}
                  </h3>
                  <div style="margin-left: 30px">
                    <h6 class="text-muted">{{resume.period}}</h6>
                    <h5>{{resume.institution}}</h5>
                    <p>
                        {{resume.description}}
                    </p>
                  </div>
                </div>
              </div>
            </li>
            
            <br />
          </ul>
        </div>
      </div>
      <div class="loaderr justify-content-center" v-else>
          <div class="loader">

          </div>
      </div>
    </div>
  </section>
</template>

<script>
export default {
  data() {
    return { resumes : null,};

  },

      mounted() {
    fetch("https://kagisomphayiportfolio.herokuapp.com/resume")
      .then((res) => res.json())
      .then(data => {
        console.log(data);
        this.resumes = data;
      });
  },
    };
    
</script>

<style scoped>
/* LOADER */
.loader {
    z-index: 1000;
  border: 8px solid #f3f3f3;
  border-radius: 50%;
  border-top: 8px solid rgba(115, 179, 106, 0.966);
  width: 60px;
  height: 60px;
  -webkit-animation: spin 2s linear infinite; /* Safari */
  animation: spin 2s linear infinite;
}

/* Safari */
@-webkit-keyframes spin {
  0% { -webkit-transform: rotate(0deg); }
  100% { -webkit-transform: rotate(360deg); }
}

@keyframes spin {
  0% { transform: rotate(0deg); }
  100% { transform: rotate(360deg); }
}
.loaderr{
    height: 80vh;
    display: flex;
    align-items: center;
}
/* LOADER END */
/* SLIDE */
 .slide{
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
/* SLIDE END */
.box-shadow{
    box-shadow: -11px 11px 13px -8px rgba(115, 179, 106, 0.966);
  -webkit-box-shadow: -11px 11px 13px -8px rgba(115, 179, 106, 0.966);
  -moz-box-shadow: -11px 11px 13px -8px rgba(95, 225, 124, 0.75);
  border: none;
}
.green{
  color: rgba(115, 179, 106, 0.966);
}
ul.timeline {
  list-style-type: none;
  position: relative;
}

ul.timeline:before {
  content: " ";
  background: #d4d9df;
  display: inline-block;
  position: absolute;
  left: 29px;
  width: 2px;
  height: 100%;
  z-index: 6;
}
ul.timeline > li {
  margin: 20px 0;
  padding-left: 20px;
}
ul.timeline > li:before {
  content: " ";
  background:  rgba(115, 179, 106, 0.966);
  display: inline-block;
  position: absolute;
  border-radius: 50%;
  border: 10px solid  rgba(115, 179, 106, 0.966);
  left: 20px;
  width: 20px;
  height: 20px;
  z-index: 8;
}
.resu {
  width: 90%;
  border-radius: 15px;
}
    @media all and (max-width: 991px) {
    .resu {
      width: 100%;
      border-radius: 15px;
    }
    
    }
</style>
