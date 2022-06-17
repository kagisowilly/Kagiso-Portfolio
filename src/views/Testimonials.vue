<template>
  <!-- Testimonials -->
  <section class="testimonial-background" id="testimonials">
    <h1 class="text-center display-6 mb-5 green fw-bold subtitlee">
      <u>TESTIMONIALS</u>
    </h1>
    <div v-if="testimonials" class="d-flex main-div align-items-center">
    <div  class="container loop">
      <div
        id="carouselExampleControlsNoTouching"
        class="carousel testi slide text-black col-lg-10"
        data-bs-touch="false"
        data-bs-interval="false"
      >
        <div class="row text-center card-shadow">
          <div
            class="carousel-inner text-black slider"
            v-for="(testimonial, index) in testimonials"
            :key="index"
          >
            <div
              class="carousel-item mt-5"
              :class="{ active: index == isActive }"
            >
              <img
                :src="testimonial.image"
                class="d-block imaage img-thumbnail"
                alt="..."
              />
              <div class="text-center mt-5">
                <p class="h5 names text-center mt-3">{{ testimonial.name }}</p>
                <div class="role-desc m-auto">
                  <b class="roles">{{ testimonial.role }}</b>
                  <div class="">
                    <p class="text-center desc mt-3">
                      {{ testimonial.description }}
                    </p>
                  </div>
                </div>
              </div>
            </div>
          </div>
          <button
            class="carousel-control-prev"
            type="button"
            @click="changePrevTesimonial"
            data-bs-target="#carouselExampleControlsNoTouching"
            data-bs-slide="prev"
          >
            <span class="carousel-control-prev-icon" aria-hidden="true"></span>
            <span class="visually-hidden">Previous</span>
          </button>
          <button
            class="carousel-control-next"
            type="button"
            @click="changeNextTesimonial"
            data-bs-target="#carouselExampleControlsNoTouching"
            data-bs-slide="next"
          >
            <span class="carousel-control-next-icon" aria-hidden="true"></span>
            <span class="visually-hidden">Next</span>
          </button>
        </div>
      </div>
    </div>      
    </div>

    <div class="loaderr justify-content-center" v-else>
      <div class="loader"></div>
    </div>
  </section>
</template>

<script>
export default {
  data() {
    return {
      isActive: 0,
      testimonials: null
    }
  },
  methods: {
    changeNextTesimonial() {
      if (this.isActive < 5) this.isActive++
      else this.isActive = 0
    },
    changePrevTesimonial() {
      if (this.isActive < 6) {
        this.isActive--
      }
      if (this.isActive < 0) {
        this.isActive = 5
      }
    }
  },

  mounted() {
    fetch('https://kagisomphayiportfolio.herokuapp.com/testimonials')
      .then((res) => res.json())
      .then((data) => {
        console.log(data)
        this.testimonials = data
      })
  }
}
</script>

<style scoped>
.main-div{
  height: 85vh;
}
.card-shadow {
  box-shadow: -11px 11px 13px -8px rgba(115, 179, 106, 0.966);
  -webkit-box-shadow: -11px 11px 13px -8px rgba(115, 179, 106, 0.966);
  -moz-box-shadow: -11px 11px 13px -8px rgba(95, 225, 124, 0.75);
  border: none;
}
.green {
  color: rgba(115, 179, 106, 0.966);
}
/* SLIDE */
.slider {
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
.carousel-inner {
  position: relative;
  width: 100%;
  overflow: auto;
}
#testimonials {
  height: 100vh;
}
.d-block {
  border-radius: 50%;
  height: 200px;
  margin: auto;
  width: 200px;
  object-fit: cover;
}
.carousel-item {
  /* background-color: #d4d9df; */
  border-radius: 15px;
  height: 500px;
}

.carousel-control-prev-icon {
  background-color: #12613b;
  margin-bottom: 230px;
}
.carousel {
  margin: 0 auto;
}
.role-desc {
  width: 70%;
}
.carousel-control-prev {
  opacity: 0.3 !important;
}
.carousel-control-next {
  opacity: 0.3 !important;
}
.carousel-control-next-icon {
  background-color: #12613b;
  margin-bottom: 230px;
}

.roles {
  color: rgba(115, 179, 106, 0.966);
  font-size: large;
  font-style: italic;
}

.names {
  font-size: x-large;
  font-weight: 700;
}

.loop {
  width: 95%;
}

.carousel-control-next-icon:hover {
  background-color: rgba(115, 179, 106, 0.966);
}
.carousel-control-prev-icon:hover {
  background-color: rgba(115, 179, 106, 0.966);
}
.description {
  width: 700px !important
  ;
}
/* MEDIA QUERIES */
@media all and (max-width: 991px) {
}
@media all and (max-width: 767px) {
  .carousel-control-prev-icon {
    margin-bottom: 280px;
    width: 30px !important;
    height: 30px !important;
  }
  .carousel-control-next-icon {
    margin-bottom: 280px;
    width: 30px !important;
    height: 30px !important;
  }
  .names {
    font-size: large;
  }
  .d-block {
    height: 190px;
    width: 190px;
  }
  .roles {
    font-size: large;
  }
  .role-desc {
    width: 80%;
  }
}
@media all and (max-width: 576px) {
  .carousel-control-prev-icon {
    margin-bottom: 280px;
    width: 30px !important;
    height: 30px !important;
  }
  .carousel-control-next-icon {
    margin-bottom: 280px;
    width: 30px !important;
    height: 30px !important;
  }
  .names {
    font-size: large;
  }
  .d-block {
    height: 140px;
    width: 140px;
  }
  .roles {
    font-size: medium;
  }
  .carousel-item {
    height: 550px;
  }
  .role-desc {
    width: 90%;
  }
}
@media all and (max-width: 461px) {
  .carousel-control-prev-icon {
    margin-bottom: 280px;
    width: 25px !important;
    height: 25px !important;
  }
  .carousel-control-next-icon {
    margin-bottom: 280px;
    width: 25px !important;
    height: 25px !important;
  }
  .names {
    font-size: medium;
  }
  .d-block {
    height: 120px;
    width: 120px;
  }
  .roles {
    font-size: medium;
    line-height: normal;
  }
  .desc {
    line-height: normal;
  }
  .role-desc {
    width: 95%;
  }
}
@media all and (max-width: 330px) {
  .carousel-control-prev-icon {
    margin-bottom: 280px;
    width: 25px !important;
    height: 25px !important;
  }
  .carousel-control-next-icon {
    margin-bottom: 280px;
    width: 25px !important;
    height: 25px !important;
  }
  .names {
    font-size: medium;
  }
  .d-block {
    height: 100px;
    width: 100px;
  }
  .roles {
    font-size: medium;
    line-height: normal;
  }
  .desc {
    line-height: normal;
  }
  .role-desc {
    width: 100%;
  }
}
</style>
