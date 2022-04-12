<template>
  <!-- projects section -->
  <section id="projects" class="projects">
    <div class="container">
                <h1 class="text-center display-6 green fw-bold subtitlee">
          <u>Projects</u>
        </h1>
        <p class="text-center text-muted mb-5">
          Below are some of the projects I've done
        </p>
      <div v-if="projects" class="pb-5 justify-content-center">

        <div  class="slide">
          <div class="row col-lg-12 proji" style="row-gap: 30px">
            <div
              v-for="project of projects"
              :key="project.title"
              class="col-lg-3 col-md-6"
              style="display: flex; justify-content: center"
            >
              <div class="card ani-card card-shadow" style="width: 18rem">
                <img :src="project.img" class="card-img-top" alt="..." />
                <div class="card-body">
                  <h4 class="card-title text-black">{{ project.title }}</h4>
                  <p class="card-text text-black">{{ project.description }}</p>
                </div>

                <div class="card-body card-icons">
                  <a target="_blank" :href="project.netlify" class="card-link">
                    <button class="mt-0 rounded">
                      <img
                        class="icon"
                        src="@/assets/netlify.png"
                        alt="Netlify"
                      />
                    </button>
                  </a>
                  <a target="_blank" :href="project.github" class="card-link">
                    <button class="mt-0 rounded">
                      <img
                        class="icon"
                        src="@/assets/githubicon.png"
                        alt="Github"
                      />
                    </button>
                  </a>
                </div>
              </div>
            </div>
          </div>
        </div>

      </div>
              <div class="loaderr justify-content-center" v-else>
          <div class="loader"></div>
        </div>
    </div>
  </section>
</template>

<script>
export default {
  data() {
    return {
      projects: null
    }
  },
  mounted() {
    fetch('https://kagisomphayiportfolio.herokuapp.com/projects')
      .then((res) => res.json())
      .then((data) => {
        console.log(data)
        this.projects = data
      })
  }
}
</script>

<style scoped>
/* LOADER */
.loader {
  z-index: 1000;
  border: 16px solid #f3f3f3;
  border-radius: 50%;
  border-top: 16px solid rgba(115, 179, 106, 0.966);
  width: 120px;
  height: 120px;
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
.icon {
  width: 40px;
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
.green {
  color: rgba(115, 179, 106, 0.966);
}
.card-shadow {
  box-shadow: -11px 11px 13px -8px rgba(115, 179, 106, 0.966);
  -webkit-box-shadow: -11px 11px 13px -8px rgba(115, 179, 106, 0.966);
  -moz-box-shadow: -11px 11px 13px -8px rgba(95, 225, 124, 0.75);
  border: none;
}
button {
  background-color: transparent;
  border: none;
}
.card-icons {
  justify-content: center;
  display: flex;
  flex-wrap: wrap;
}

.icon:hover {
  -ms-transform: scale(1.5); /* IE 9 */
  -webkit-transform: scale(1.5); /* Safari 3-8 */
  transform: scale(1.5);
}
.card {
  width: 50%;
  height: 410px;
}

.card-body {
  overflow: auto;
  text-align: center;
}
.card-img-top {
  height: 150px;
  width: 100%;
}
</style>
