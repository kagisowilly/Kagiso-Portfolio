<template>
  <!-- LANDING SECTION -->
  <section class="num-one" id="home">
    <!-- Landing-->
    <div class="container one">
      <div class="row home-content" >
        <div class="col- text-center">
          <h1 style="color: rgba(115, 179, 106, 0.966)" class="display-1 main-title fw-bold">
            Kagiso Mphayi
          </h1>
          <div class="col-lg-6 mx-auto">
            <div class="lead text-white">
              <p class="mt-3 text-white">
                <span>| Junior Front-end Developer|</span>
                <span> Designer |</span>
                <span> Photographer |</span>
              </p>
            </div>
            <div class="d-grid gap-4 d-flex home-icon justify-content-center">
              <a
                target="_blank"
                href="https://www.linkedin.com/in/kagiso-kagiso-5aab71219/"
                class="text-white icons"
                ><i class="bi icn social-icon bi-linkedin"></i
              ></a>
                <a
                target="_blank"
                href="https://github.com/Kagisowilly"
                class="text-white icons"
                ><i class="bi icn social-icon bi-github"></i
              ></a>
              <a
                target="_blank"
                href="https://twitter.com/K_Mphayi"
                class="text-white icons"
                ><i class="bi icn social-icon bi-twitter"></i
              ></a>
            </div>
          </div>
        </div>

      </div>
    </div>
    <div class="text-center"></div>
  </section>
</template>

<script>


export default {

}
</script>

<style scoped>
    .icons {
      font-size: 30px;
    }

    .main-title{
      font-size: 120px;
      margin-top: 0px !important;
    }
    .home-content{
display: flex;
align-items: center;
height: 100vh;
justify-content: center;
      }
.boot-arrow {
  font-size: 25px;
  color:rgba(115, 179, 106, 0.966);
}
.boot-arrow:hover{
  color: black;
}


.icons:hover{
  -ms-transform: scale(1.5);
  -webkit-transform: scale(1.5);
  transform: scale(1.5); 
}
   .num-one {
    height: 100vh;
    margin-top: 0;
    background-image: url("/assets/background.jpeg");
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
   @media all and (max-width: 992px) {
    .main-title{
font-size: 80px !important;
    }
    p{font-size: 15px;}
   }
      @media all and (max-width: 768px) {
    .main-title{
      font-size: 50px !important;
    }
    p{font-size: 30px;}
   }
      @media all and (max-width: 576px) {
    .main-title{
      font-size: 50px !important;
    }
    p{font-size: 15px;}
   }

</style>
