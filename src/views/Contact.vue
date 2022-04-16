<template>
  <section class="contact-background" id="contact">
    <h2 class="text-center green display-6 fw-bold mb-3 subtitlee">
      <u>Contact Me</u>
    </h2>  
    <div class="cont">
      <div class="formm container justify-content-center">
        <div class="row">
          <div class="col-md-6 sliderrr col-sm-12 col- col-lg-4 col-12">
            <div class=" ">
              <label><h5><i class="bi bi-envelope contact-icons"></i>  Email:</h5></label>
              <p>mphayiw@gmail.com</p>

              <label><h5><i class="bi bi-telephone contact-icons"></i>Contact number:</h5></label>
              <p>(+27)79 928 2407</p>
              <label> <h5><i class="bi bi-geo-alt contact-icons"></i>Adress:</h5></label>
              <p>
                Firgrove Rural
                <br />
                Cape Town, South Africa
              </p>
            </div>
          </div>

          <div class=" form-cont  col-md-6 col-sm-12 col- col-lg-8 col-12">
            <form @submit.prevent="handleSubmit" class="contactMe card-shadow slider container">
              <div id="emailHelp" class="form-text text-center">
                <p>
                  Let's get in touch.
                  <br />
                  I will never share your information with anyone.
                </p>
              </div>
              <label class="text-black">Name:</label>
              <input
                class="form-input neu-border-inset"
                type="text"
                v-model="name"
                required
              />
              <label class="text-black">Email:</label>
              <input
                class="form-input neu-border-inset"
                type="email"
                v-model="email"
                required
              />

              <label class="text-black">Subject:</label>
              <input
                class="form-input neu-border-inset"
                type="text"
                v-model="subject"
              />

              <label class="text-black">Message:</label>
              <input
                class="form-input message-input neu-border-inset"
                type="text"
                v-model="message"
                required
              />

              <div class="submit mb-3">
                <button type="Submit" class="mb-3 btn button-body">
                  <h5 id="sub" class="text-black mb-0">Submit</h5>
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
.card-shadow {
  box-shadow: -11px 11px 13px -8px rgba(115, 179, 106, 0.966);
  -webkit-box-shadow: -11px 11px 13px -8px rgba(115, 179, 106, 0.966);
  -moz-box-shadow: -11px 11px 13px -8px rgba(95, 225, 124, 0.75);
  border: none;
}
.green {
  color: rgba(115, 179, 106, 0.966);
}

h5 {
  color: rgba(115, 179, 106, 0.966);
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
  margin: 25px 0 15px;
  text-transform: uppercase;
  letter-spacing: 1px;
  font-weight: bold;
}
input {
  display: block;
  padding: 10px 6px;
  width: 100%;
  box-sizing: border-box;
  border: 1px solid #ddd;
  color: rgb(0, 0, 0);
  background-color: rgba(233, 221, 221, 0.25);
}
.button-body {
  background: rgba(115, 179, 106, 0.966);
  border: 0;
  padding: 10px 20px;
  margin-top: 20px;
  color: rgb(255, 255, 255);
  border-radius: 10px;
  cursor: pointer;
  margin-bottom: 50px !important;
}
button:hover {
  opacity: 0.8;
  background: rgba(10, 81, 139, 0.979);
}
.submit {
  text-align: center;
}
#sub:hover {
  color: rgb(255, 255, 255) !important;
}
#sub {
  color: white;
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
}
.contact-icons {
  font-size: 20px !important;
}
.formm {
  width: 100%;
  height: 100vh;
  padding-top: 70px;
}
.cont {
  display: flex;
  flex-wrap: wrap;
  justify-content: center !important;
  padding-bottom: 40px;
}
/* SLIDE LEFT */
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
    margin-left: 50%;
    width: 100%;
  }
}

/* SLIDE END */

/* SLIDE RIGHT */
.sliderrr {
  animation-duration: 1s;
  animation-name: slideiner;
}
template {
  background-color: #f2f2fc;
}
@keyframes slideiner {
  from {
    margin-left: -50%;
    width: 100%;
  }

  to {
    margin-right: 0%;
    width: 0%;
  }
}

/* SLIDE END */
@media all and (max-width: 800px) {
  .formm {
    width: 100%;
  }
}
</style>
