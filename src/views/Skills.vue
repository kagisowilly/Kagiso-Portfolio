<template>
  <section id="skills" style="">
    <h1 class="text-center display-6 subtitlee fw-bold"><u>Skills</u></h1>

    <div class="container skills-content col-lg-12 mt-5">
      <div class="">
          
        <div class="bar">
  <div class="rating slide" style="height:24px;width:25%"></div>
</div><br>

<div class="bar">
  <div class=" rating slide" style="height:24px;width:50%"></div>
</div><br>

<div class="bar">
  <div class=" rating slide" style="height:24px;width:75%"></div>
</div><br>

        <div class="bar">
  <div class=" rating slide" style="height:24px;width:25%"></div>
</div><br>
        <div class="bar">
  <div class="rating slide" style="height:24px;width:25%"></div>
</div><br>

<div class="bar">
  <div class=" rating slide" style="height:24px;width:50%"></div>
</div><br>

<div class="bar">
  <div class=" rating slide" style="height:24px;width:75%"></div>
</div><br>

        <div class="bar">
  <div class=" rating slide" style="height:24px;width:25%"></div>
</div><br>

</div>
    </div>
  </section>
</template>

<script>
export default {};
</script>

<style scoped>
/* .skills-content{
    display: flex;
    align-items: center;
    height: 100vh;
} */
.rating{
    background-color: rgba(115, 179, 106, 0.966);
}
.bar{
    background-color: rgb(223, 223, 223);
}
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
    margin-left: 0%;
    width: 0%;
  }

  to {
    margin-right: 0%;
    max-width: 100%;
  }
}
/* SLIDE END */
</style>
