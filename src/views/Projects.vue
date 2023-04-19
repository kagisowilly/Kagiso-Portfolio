<template>
  <!-- projects section -->
  <section id="projects" class="projects">
    <div class="container">
      <h1 class="text-center display-6 fw-bold subtitlee">
        <u>PROJECTS</u>
      </h1>
      <p class="text-center text-muted mb-5">
        Below are some of my personal projects.
      </p>
      <div v-if="projects" class="pb-5 justify-content-center">
        <div class="slide">
          <div class="row col-lg-12 proji" style="row-gap: 30px">
            <div
              class="col-lg-3 col-md-6 col-sm-12"
              v-for="project of projects"
              :key="project.title"
            >
              <!-- items -->
              <div class="card-shadow menu-item">
                <div class="image-div">
                  <img class="imaage" :src="project.img" alt="food image" />
                </div>

                <div class="menu-overlay">
                  <div class="menu-overlay-content">
                    <div>
                      <h6 class=" green mb-1">{{ project.title }}</h6>
                    </div>
                    <span class="text-white span">{{ project.description }}</span>

                    <div class="card-icons">
                      <a
                        target="_blank"
                        :href="project.netlify"
                        class="card-link"
                      >
                        <button class="mt-0 rounded">
                          <img
                            class="icon"
                            src="@/assets/netlify.png"
                            alt="Netlify"
                          />
                        </button>
                      </a>
                      <a
                        target="_blank"
                        :href="project.github"
                        class="card-link"
                      >
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
                <!-- </a> -->
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
    fetch('https://kagisoportfolio.onrender.com/projects',{mode: 'cors'})
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
.icon {
  width: 30px;
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
  font-weight: bolder;
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
  -ms-transform: scale(1.2); /* IE 9 */
  -webkit-transform: scale(1.2); /* Safari 3-8 */
  transform: scale(1.2);
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

/* SEKO CSS */
.image-div {
  width: 100%;
}
.imaage {
  height: 310px;
  object-fit: cover;
  overflow: hidden;
  width: 100%;
}
.first-menu {
  display: flex;
  gap: 10px;
  margin: 5px;
}
.second-menu {
  display: flex;
  margin: 5px;
  gap: 10px;
}
.title {
  padding: 0.2rem;
}
.menu-wrapper {
  margin-top: 2rem;
  display: flex;
  flex-direction: row;
  flex-wrap: wrap;
}
.menu-item {
  position: relative;
  cursor: pointer;
}
.menu-overlay {
  height: 60%;
  background: rgba(0, 0, 0, 0.8);
  position: absolute;
  bottom: 0;
  width: 100%;
  color: #fff;
  padding: 1.5rem;
  opacity: 0;
  transition: var(--transition);
  overflow: hidden;
}
.menu-overlay-content {
  overflow: hidden;
  transition: all 0.5s ease;
  transform: translateY(100%);
  text-size-adjust: 40px;
  position: absolute;
  bottom: 0;
}
.menu-overlay-content div {
  display: flex;
  justify-content: space-between;
}
.edit-btn {
  display: inline-block;
  justify-content: space-around;
}
.menu-overlay-content h2 {
  text-transform: capitalize;
  margin-bottom: 0;
  margin-bottom: -6px;
}
.menu-overlay-content {
  text-transform: uppercase;
  color: var(--grey);
  margin-top: 0.6rem;
  font-size: 0.8rem;
  font-size: x-small;
  margin-bottom: 0px;
}
.menu-item:hover .menu-overlay {
  opacity: 1;
}
.menu-item:hover .menu-overlay-content {
  transform: translateY(0);
}
.border {
  width: 100%;
  align-items: center;
  text-align: center;
  border-bottom: 4px solid var(--grey);
}

</style>
