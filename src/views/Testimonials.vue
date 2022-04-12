<template>
  <!-- Testimonials -->
  <section class="testimonial-background" id="testimonials">
    <h1 class="text-center display-6 mb-5 green fw-bold subtitlee">
      <u>Testimonials</u>
    </h1>
    <div v-if="testimonials" class="container ">
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
                class="d-block img-thumbnail"
                alt="..."
              />
              <div class="text-center mt-5">
                <p class="h5 names text-center mt-3">{{ testimonial.name }}</p>
                <b class="roles">{{ testimonial.role }}</b>
                <div class=" ">
                  <p class="text-center mt-3">{{ testimonial.description }}</p>
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
  background-color: rgba(115, 179, 106, 0.966);
  margin-bottom: 230px;
}
.carousel {
  margin: 0 auto;
}

.carousel-control-prev {
  opacity: 0.3 !important;
}
.carousel-control-next {
  opacity: 0.3 !important;
}
.carousel-control-next-icon {
  background-color: rgba(115, 179, 106, 0.966);
  margin-bottom: 230px;
}

.roles {
  color: rgba(115, 179, 106, 0.966);
  font-size: x-large;
}

.names {
  font-size: xx-large;
}

.carousel-control-next-icon:hover {
  background-color: white;
}
.carousel-control-prev-icon:hover {
  background-color: white;
}
.description {
  width: 700px !important
  ;
}
</style>
