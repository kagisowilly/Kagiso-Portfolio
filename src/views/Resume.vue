<template>
  <!-- RESUME -->

  <section class="education-work" id="education">
    <h1 class="text-center display-6 fw-bold subtitlee ">
      <u>RESUME</u>
    </h1>
    <h5 class="text-center edu-resu mb-5 ">EDUCATION | EXPRERIENCE</h5>
    <div class="container mb-5">
      <div class="row justify-content-center" v-if="resumes">
        <div class="col-lg-10 text-black">
          <ul class="timeline">
            <!-- LOOPING -->
            <li class="slide" v-for="resume of resumes" :key="resume.title">
              <div class="resu box-shadow">
                <div class="p-2">
                  <h5 class="green title">
                    <i class="bi bi-calendar-fill"></i>
                    {{ resume.title }}
                  </h5>
                  <div style="margin-left: 30px">
                    <h6 class="text-muted period">{{ resume.period }}</h6>
                    <h6>{{ resume.institution }}</h6>
                    <p class="description">
                      {{ resume.description }}
                    </p>
                  </div>
                </div>
              </div>
            </li>
            <br />
          </ul>
        </div>
      </div>
      <!-- LOADER -->
      <div class="loaderr justify-content-center" v-else>
        <div class="loader"></div>
      </div>
    </div>
  </section>
</template>

<script>
export default {
  data() {
    return { resumes: [
    {
      id: 1,
      title: "JUNIOR WEB DEVELOPER",
      period: "October(2022) - Present(2023)",
      description: ``,
      institution: "CIMSO",
    },
    {
      id: 2,
      title: "JUNIOR WEB DEVELOPER",
      period: "August(2022) - September(2022)",
      description: `Before the company got restructured and our department getting dissolved, I worked as a junior web developer,
       a support to the senior developer. Some of my roles included Strategizing with the design team about all online user experience, from
       conceptualizing, site mapping, wire-framing and implementing, WordPress development, migrating websites to new servers, Website maintenance- maintaining our sites each month with software
       updates.`,
      institution: "Dlonra Pty",
    },
    {
    id: 3,
    title: "ASSISTANT LECTURER",
    period: "April(2022) - July(2022)",
    description: `The role included 
    clarifying the course content (JavaScript, Bootstrap, HTML, CSS, Vue.js, Node.js(express), MongoDB, and MySQL.) to the students individually or in groups,
     supporting the lecturing team with technical requirements on a day-to-day
    basis,
    giving feedback on any challenges that might arise on a daily basis with
students to leadership and facilitators,
assisting in identifying potential opportunities for improvements within the
curriculum and overall implementation of the coding program,
assisting with marking of modules and tasks and assisting with managing and updating the student portal when needed.
    `,
    institution: "LifeChoices Coding Academy",
  },
    {
      id: 4,
      title: "WEB DEVELOPMENT",
      period: "September(2021) - March(2022)",
      description: `Life Choices is a year-long bootcamp where we learn more about Web development and its fundamentals. We also get the oppotunity to learn interpersonal skills.`,

      institution: "LifeChoices Coding Academy",  
    },

    {
      id: 5,
      title: "CUSTOMER SERVICE",
      description: `I was offered the opportunity to learn the importance of strong and consistent communication; how to handle difficult customers; how to handle complaints; and the value of loyalty in the work place.`,
      institution: "eLearning College",
      period: "August(2021)",
    },
    {

      id: 6,
      title: "PRIVATE TUTORING|SELF-LEARNING",
      description: `Throughout the year, I tutored the grade 12 learners from my area maths and physics, and I also used the time in between to
                    teach myself HTML and CSS with the clear help
                    of online resources.`,
      institution: "",
      period: "February 2020 - November 2020",
    },
    {
      id: 7,
      title: "ASSISTING FIRST-YEAR STUDENTS",
      description: `I was assisting first-year Students at the University Of Pretoria with online registration and using peripheral equipment.`,
      institution: "",
      period: "January-February(2018) & January-February(2019)",
    }
    ,
    {
      id: 8,
      title: "PRIVATE TUTORING",
      description: `During this period I was tutoring some of the grade 12
                  learners from my area maths and physics. The experience
                  helped me a lot with improving my communication skills.`,
      institution: "",    
      period: "February 2015 - November 2015",
    },
    {
      id: 9,
      title: "NATIONAL SENIOR CERTIFICATE",
      description: `During my time at this institution I improved my social skills, and worked more on my time management.`,
      institution: "Mmametlhake High School", 
      period: "January 2012 - December 2014",
    }
  ]}
  },
// FETCHING FROM AN API
  // mounted() {
  //   fetch('https://kagisoportfolio.onrender.com/resume',{mode: 'cors'})
  //     .then((res) => res.json())
  //     .then((data) => {
  //       console.log(data)
  //       this.resumes = data
  //     })
  // }
}
</script>

<style scoped>
/* LOADER */
  h6{
        font-weight: 600;
  }
  .edu-resu{
font-weight: bold;
  }
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
  0% {
    -webkit-transform: rotate(0deg);
  }
  100% {
    -webkit-transform: rotate(360deg);
  }
}

@keyframes spin {
  0% {
    transform: rotate(0deg);
  }
  100% {
    transform: rotate(360deg);
  }
}
.loaderr {
  height: 80vh;
  display: flex;
  align-items: center;
}
/* LOADER END */
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

/* BOX */
.box-shadow {
  box-shadow: -11px 11px 13px -8px rgba(115, 179, 106, 0.966);
  -webkit-box-shadow: -11px 11px 13px -8px rgba(115, 179, 106, 0.966);
  -moz-box-shadow: -11px 11px 13px -8px rgba(95, 225, 124, 0.75);
  border: none;
}
.resu {
  width: 90%;
  border-radius: 15px;
}
/* FONT */
.green {
  color: rgba(115, 179, 106, 0.966);
  font-size: 1em;
  font-weight: bolder;
}
/* TIMELINE */
ul.timeline {
  list-style-type: none;
  position: relative;
}

ul.timeline:before {
  content: ' ';
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
  content: ' ';
  background: rgba(115, 179, 106, 0.966);
  display: inline-block;
  position: absolute;
  border-radius: 50%;
  border: 10px solid rgba(115, 179, 106, 0.966);
  left: 20px;
  width: 20px;
  height: 20px;
  z-index: 8;
}
/* MEDIA QUERIES */
@media all and (max-width: 991px) {
}
@media all and (max-width: 767px) {
}
@media all and (max-width: 576px) {
  .edu-resu{
    font-size: 15px;
    padding-top: 10px !important ;
  }
  .title{
    font-size: 15px;
  }
  .period{
    font-size: 13px;
  }
  h5{
    font-size: 15px;
    font-weight: bold;
  }
  .description{
    line-height: 120%;
  }
}
@media all and (max-width: 461px) {
}
@media all and (max-width: 330px) {
}
</style>
