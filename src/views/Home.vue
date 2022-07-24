<template>
  <!-- LANDING SECTION -->
  <section class="num-one" id="home">
    <div class="container one">
      <div class="row home-content">
        <div class="col- text-center">
          <div class="myname">
            <h4
              style="color: rgba(115, 179, 106, 0.966)"
              class="display-1 main-title2 fw-bold"
            >
              Hi,
              <span style="color: rgba(255, 255, 255)">I'm</span>
            </h4>
            <h1
              style="color: rgba(115, 179, 106, 0.966)"
              class="display-1 main-title fw-bold"
            >
              Kagiso Mphayi
            </h1>
          </div>
          <div class="col-lg-6 mx-auto">
            <div class="lead text-white">
              <p class="mt-3 text-white">
                <span class="text-white span typed-text">{{ typeValue }}</span>
                <span class="cursor span text-white" :class="{ typing: typeStatus }">
                  &nbsp;
                </span>
              </p>
            </div>
            <!-- ICONS -->
            <div class="d-grid gap-4 d-flex home-icon justify-content-center">
              <a
                target="_blank"
                href="https://www.linkedin.com/in/kagiso-mphayi-5aab71219/"
                class="text-white icons"
              >
                <i class="bi icn social-icon bi-linkedin"></i>
              </a>
              <a
                target="_blank"
                href="https://github.com/Kagisowilly"
                class="text-white icons"
              >
                <i class="bi icn social-icon bi-github"></i>
              </a>
              <a
                target="_blank"
                href="https://twitter.com/K_Mphayi"
                class="text-white icons"
              >
                <i class="bi icn social-icon bi-twitter"></i>
              </a>
            </div>
          </div>
        </div>
      </div>
    </div>
    <div class="text-center"></div>
  </section>
</template> 
|

<script>
import { setTimeout } from 'timers'
export default {
  data: () => {
    return {
      typeValue: '',
      typeStatus: false,
      typeArray: ['Junior Full Stack Developer', 'Designer', 'Photographer'],
      typingSpeed: 100,
      erasingSpeed: 100,
      newTextDelay: 1000,
      typeArrayIndex: 0,
      charIndex: 0
    }
  },
  methods: {
    typeText() {
      if (this.charIndex < this.typeArray[this.typeArrayIndex].length) {
        if (!this.typeStatus) this.typeStatus = true

        this.typeValue += this.typeArray[this.typeArrayIndex].charAt(
          this.charIndex
        )
        this.charIndex += 1

        setTimeout(this.typeText, this.typingSpeed)
      } else {
        this.typeStatus = false
        setTimeout(this.eraseText, this.newTextDelay)
      }
    },
    eraseText() {
      if (this.charIndex > 0) {
        if (!this.typeStatus) this.typeStatus = true

        this.typeValue = this.typeArray[this.typeArrayIndex].substring(
          0,
          this.charIndex - 1
        )
        this.charIndex -= 1
        setTimeout(this.eraseText, this.erasingSpeed)
      } else {
        this.typeStatus = false
        this.typeArrayIndex += 1
        if (this.typeArrayIndex >= this.typeArray.length)
          this.typeArrayIndex = 0

        setTimeout(this.typeText, this.typingSpeed + 1000)
      }
    }
  },
  created() {
    setTimeout(this.typeText, this.newTextDelay + 200)
  }
}
</script>

<style scoped>
/* ICONS */
.icons {
  font-size: 25px;
}
.icons:hover {
  -ms-transform: scale(1.5);
  -webkit-transform: scale(1.5);
  transform: scale(1.5);
  color: rgba(115, 179, 106, 0.966) !important;
}
/* TEXT */
p {
  font-size: 30px;
}

.main-title {
  font-size: 120px;
  margin-top: 0px !important;
}
.main-title2 {
  font-size: 60px;
  margin-top: 0px !important;
}
/* HOME CONTENT POSITIONING */
.home-content {
  display: flex;
  align-items: center;
  height: 100vh;
  justify-content: center;
}
/* BACKGROUND IMAGE */
.num-one {
  height: 100vh;
  margin-top: 0;
  background-image: url('/assets/background.jpeg');
  background-repeat: no-repeat;
  background-size: cover !important;
  background-image: linear-gradient(
      0deg,
      rgba(0, 0, 0, 0.2),
      rgba(0, 0, 0, 0.2)
    ),
    url(../assets/background.jpeg);
  overflow-x: hidden;
  overflow-y: hidden;
  background-position: 70%;
}
/* MEDIA QUERIES */
@media all and (max-width: 992px) {
  .main-title {
    font-size: 80px !important;
  }
  .main-title2 {
    font-size: 50px !important;
  }
  p {
    font-size: 25px;
  }
}
@media all and (max-width: 768px) {
  .main-title {
    font-size: 50px !important;
  }
  .main-title2 {
    font-size: 50px !important;
  }
  p {
    font-size: 20px;
  }
}
@media all and (max-width: 576px) {
  .main-title {
    font-size: 70px !important;
  }
  .main-title2 {
    font-size: 35px !important;
  }
  p {
    font-size: 15px;
  }
}
@media all and (max-width: 350px) {
  .main-title {
    font-size: 50px !important;
  }
  .main-title2 {
    font-size: 35px !important;
  }
  p {
    font-size: 12px;
  }
}

/* ANIMATION */
@keyframes cursorBlink {
  49% {
    background-color: #fff;
  }
  50% {
    background-color: transparent;
  }
  99% {
    background-color: transparent;
  }
}
</style>
