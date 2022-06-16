<template>
  <section class=" contact-background" id="contact">
    <h2 class="text-center green display-6 fw-bold mb-3 subtitlee">
      <u>CONTACT</u>
    </h2>
    <h5 class="text-center span">LET'S GET IN TOUCH</h5>
    <div class="cont slide">
      <div class="formm container justify-content-center">
        <div class="row">
          <div class="col-md-6 sliderrr col-sm-12 col- col-lg-4 col-12">
            
            <h5 class="span2">LET'S GET IN TOUCH</h5>

            <hr>
            <div class=" ">
              <div class="d-flex mt-4">
              <div >
              <i class="bi bi-envelope-fill icons"></i>               
              </div>
              <div class="mx-md-4 mx-sm-3 mx-1 ">
              <h6 class="mb-0">EMAIL:</h6>
              <p>
                mphayiw@gmail.com
              </p>                
              </div>                
              </div>

              <div class="d-flex my-4">
              <div >
              <i class="bi bi-telephone-fill icons"></i>               
              </div>
              <div class="mx-md-4 mx-sm-3 mx-1 ">
              <h6 class="mb-0">CONTACT NO.</h6>
              <p>
               (+27)79 928 2407 
              </p>                
              </div>                
              </div>

              <div class="d-flex">
              <div >
              <i class="bi bi-geo-alt-fill icons" ></i>               
              </div>
              <div class="mx-md-4 mx-sm-3 mx-1 ">
              <h6 class="mb-0">ADRESS:</h6>
              <p>
                Cape Town, South Africa
              </p>                
              </div>                
              </div>
            </div>
          </div>
          <div class=" form-cont  col-md-6 col-sm-12 col- col-lg-8 col-12">
            <form @submit.prevent="handleSubmit" class="contactMe card-shadow slider container">
              <div id="emailHelp" class="form-text text-center">
              </div>
              <input
                class="form-input neu-border-inset"
                type="text"
                v-model="name"
                required
                placeholder="Name*"
              />
              <input
                class=" form-input email neu-border-inset"
                type="email"
                v-model="email"
                required
                placeholder="Email*"
              />
              <input
                class="form-input neu-border-inset subject"
                type="text"
                v-model="subject"
                placeholder="Subject"
              />
              <textarea
                class=" form-input message-input neu-border-inset"
                type="text"
                v-model="message"
                required
                placeholder="Message*"
              ></textarea>

              <div class="submit mb-3">
                <button type="Submit" class="mb-3  button-body">
                  SUBMIT
                </button>
              </div>
            </form>
          </div>
        </div>
      </div>
    </div>
  </section>
</template>

<script>
export default {
  data() {
    return {
      name: '',
      email: '',
      subject: '',
      message: ''
    }
  },
  methods: {
    handleSubmit() {
      fetch('https://laundry-villa.herokuapp.com/contact', {
        method: 'POST',
        body: JSON.stringify({
          name: this.name,
          email: this.email,
          subject: this.subject,
          message: this.message
        }),
        headers: {
          'Content-type': 'application/json; charset=UTF-8'
        }
      })
        .then((response) => response.json())
        .then((data) => (this.contact = data))
      alert('Message successfully sent').catch((err) =>
        console.log(err.message)
      )
    }
  }
}
</script>

<style scoped>
/* ICONS */
.message-input, .email,.subject {
  margin-top: 30px;
}
.icons {
  font-size: 30px;
  color: rgba(115, 179, 106, 0.966) !important;

}
h5{
  font-weight: bold;
}
.green {
  color: rgba(115, 179, 106, 0.966);
}
h6 {
  color: rgba(115, 179, 106, 0.966);
  font-weight: bold;
}
.iframe {
  margin-top: 150px;
}
form {
  max-width: 100%;
  margin: 30px auto;
  text-align: left;
  border-radius: 10px;
}
label {
  color: rgb(0, 0, 0);
  display: inline-block;
  margin: 12px 0 15px;
  text-transform: uppercase;
  letter-spacing: 1px;
  font-weight: bold;
}
input, textarea{
  display: block;
  padding: 5px 3px;
  width: 100%;
  box-sizing: border-box;
  border: 1px solid #ddd;
  color: white;
  background-color: rgba(115, 179, 106, 0.966) ;
}
textarea{
  height: 10rem;
}
.button-body {
  background: rgba(115, 179, 106, 0.966);
  border: 0;
  padding: 7px 15px;
  margin-top: 30px;
  color: rgb(0, 0, 0);
  cursor: pointer;
  margin-bottom: 10px !important;
  font-weight: bold;
  letter-spacing: 1px;
}
button:hover {
  opacity: 0.8;
  background: #12613b;
  color: rgb(255, 255, 255) !important;
}

.span2{
display: block;
}
.span{
display: none !important;
}
.error {
  color: #ff0062;
  margin-top: 10px;
  font-size: 0.8em;
  font-weight: bold;
}
.contactMe {
  width: 100%;
  margin: 0px;
  padding: 0;
}
.contact-icons {
  font-size: 20px !important;
}
.formm {
  width: 100%;
}
.cont {
  display: flex;
  flex-wrap: wrap;
  justify-content: center !important;
  align-items: center !important;
  min-height: 90vh;
}
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
@media all and (max-width: 800px) {

}
@media all and (max-width: 768px) {
.span{
display: block !important;
}
.span2{
display: none;
}
}
</style>
