

<template>

  <div class="hello">
   

    <template>
      <b-container>
        <b-row>
          <!-- <div>
            <b-button v-b-modal.modal-center>Launch centered modal</b-button>

            <b-modal id="modal-center" centered title="BootstrapVue"> -->
              <!-- <p class="my-4">Vertically centered modal!</p> -->
               <div v-if="step === 1">
              <div id="popup" class="popup1_mn">
                <div class="popup_block">
                  <span class="close"></span>
                  <ul class="popup_top">
                    <div class="pop_inner">
                      <li class="active">
                        <span class="circle">
                          <span class="inner_circle"></span>
                        </span>
                        <p>How to Gift?</p>
                      </li>
                      <li>
                        <span class="circle">
                          <span class="inner_circle"></span>
                        </span>
                        <p>Details</p>
                      </li>
                      <li>
                        <span class="circle">
                          <span class="inner_circle"></span>
                        </span>
                        <p>Review</p>
                      </li>
                      <li>
                        <span class="circle">
                          <span class="inner_circle"></span>
                        </span>
                        <p>Sent!</p>
                      </li>
                    </div>
                  </ul>
                  <ul class="popup_content">
                    <li>
                      <span>1</span>
                      <div class="inner_content">
                        <h3>You send gift</h3>
                        <p>The recipient receives your gift via email with a message from you.</p>
                      </div>
                    </li>
                    <li>
                      <span>2</span>
                      <div class="inner_content">
                        <h3>They Personalize the gift</h3>
                        <p>The recipient enters their preferences (color, size, etc.) and address.</p>
                      </div>
                    </li>
                    <li>
                      <span>3</span>
                      <div class="inner_content">
                        <h3>You complete the purchase</h3>
                        <p>We’ll notify you via email when they enter their information, and then you can complete the purchase.</p>
                      </div>
                    </li>
                  </ul>
                
                  <div class="common_btn">
                    
                    <a class="begin" href="javaScript:void(0)">
                      <span>Let’s Begin</span>
                    </a>
                    <p>
                      Powered by
                      <img src="#" />
                    </p>
                  </div>
                </div>
              </div>
               </div>

              <div id="popup2" class="popup1_mn">
                <div class="popup_block popup2">
                  <span class="close"></span>
                  <ul class="popup_top">
                    <div class="pop_inner">
                      <li class="active tick">
                        <span class="circle">
                          <span class="inner_circle"></span>
                        </span>
                        <p>How to Gift?</p>
                      </li>
                      <li class="active">
                        <span class="circle">
                          <span class="inner_circle"></span>
                        </span>
                        <p>Details</p>
                      </li>
                      <li>
                        <span class="circle">
                          <span class="inner_circle"></span>
                        </span>
                        <p>Review</p>
                      </li>
                      <li>
                        <span class="circle">
                          <span class="inner_circle"></span>
                        </span>
                        <p>Sent!</p>
                      </li>
                    </div>
                  </ul>
                  <ul class="popup_content">
                    <li>
                      <label for="To" class>To</label>
                      <input
                        type="text"
                        id="RecipientName"
                        name="RecipientName"
                        v-model="form.name"
                        placeholder="Recipient Name"
                      />
                      <input
                        type="text"
                        id="RecipientEmail"
                        name="RecipientEmail"
                        v-model="form.email"
                        placeholder="Recipient Email"
                      />
                    </li>
                    <li>
                      <label for="Form" class>Form</label>
                      <input
                        type="text"
                        id="YourName"
                        name="YourName"
                        v-model="form.yname"
                        placeholder="Your Name"
                      />
                      <input
                        type="text"
                        id="YourEmail"
                        name="YourEmail"
                        v-model="form.yemail"
                        placeholder="Your Email"
                      />
                      <select id="Gift Occasion" name="Gift Occasion">
                        <option value="GiftOccasion">Gift Occasion</option>
                        <option value="Birthday">Birthday</option>
                        <option value="Anniversary">Anniversary</option>
                        <option value="Holiday">Holiday</option>
                        <option value="JustBecause">Just Because</option>
                        <option value="Graduation">Graduation</option>
                        <option value="Other">Other</option>
                      </select>
                    </li>
                    <li>
                      <label for="Message" class>Message</label>
                      <textarea
                        rows="1"
                        id="Message"
                        name="Message"
                        v-model="form.msgbox"
                        placeholder="Your Message"
                      ></textarea>
                    </li>
                  </ul>
                  <div class="common_btn">
                    <a class="back" href="javaScript:void(0)">
                      <span>Back</span>
                    </a>
                    <a class="review" href="javaScript:void(0)" @click="onSubmit" @reset="onReset">
                      <span>Review</span>
                    </a>
                    <p>
                      Powered by
                      <img src="#" />
                    </p>
                  </div>
                </div>
              </div>

              <div id="popup3" class="popup1_mn">
                <div class="popup_block popup3">
                  <span class="close"></span>
                  <ul class="popup_top">
                    <div class="pop_inner">
                      <li class="active tick">
                        <span class="circle">
                          <span class="inner_circle"></span>
                        </span>
                        <p>How to Gift?</p>
                      </li>
                      <li class="active tick">
                        <span class="circle">
                          <span class="inner_circle"></span>
                        </span>
                        <p>Details</p>
                      </li>
                      <li class="active">
                        <span class="circle">
                          <span class="inner_circle"></span>
                        </span>
                        <p>Review</p>
                      </li>
                      <li>
                        <span class="circle">
                          <span class="inner_circle"></span>
                        </span>
                        <p>Sent!</p>
                      </li>
                    </div>
                  </ul>
                  <ul class="popup_content">
                    <li>
                      <h3>To</h3>
                      <p>
                        <span>{{ nameto}}</span>
                        {{emailto}}
                      </p>
                    </li>
                    <li>
                      <h3>Form</h3>
                      <p>
                        <span>{{namefrom}}</span>
                        {{emailfrom}}
                      </p>
                    </li>
                    <li>
                      <h3>Occassion</h3>
                      <p>
                        25th Birthday
                        <br />Ceremony
                      </p>
                    </li>
                    <li>
                      <h3>Message</h3>
                      <p>{{ msgboxall}}</p>
                    </li>
                  </ul>
                  <div class="common_btn">
                    <a class="back_new" href="javaScript:void(0)">
                      <span>Back</span>
                    </a>
                    <a class="submit" href="javaScript:void(0)">
                      <span>Submit</span>
                    </a>
                    <p>
                      Powered by
                      <img src="#" />
                    </p>
                  </div>
                </div>
              </div>

              <div id="popup5" class="popup1_mn">
                <div class="popup_block popup5">
                  <span class="close"></span>
                  <ul class="popup_top popup_new">
                    <div class="pop_inner">
                      <li class="active">
                        <span class="circle">
                          <span class="inner_circle"></span>
                        </span>
                        <p>Shipping Details</p>
                      </li>
                      <li>
                        <span class="circle">
                          <span class="inner_circle"></span>
                        </span>
                        <p>Complete!</p>
                      </li>
                    </div>
                  </ul>
                  <ul class="popup_content">
                    <label for="ShippingInformation" class>Shipping Information</label>
                    <li>
                      <input
                        type="text"
                        id="FirstName"
                        name="FirstName"
                        v-model="Shippingform.fname"
                        placeholder="First Name"
                      />
                    </li>
                    <li>
                      <input
                        type="text"
                        id="LastName"
                        name="LastName"
                        v-model="Shippingform.lname"
                        placeholder="Last Name"
                      />
                    </li>
                    <li>
                      <input
                        type="text"
                        id="Company"
                        name="Company"
                        v-model="Shippingform.company"
                        placeholder="Company (optional)"
                      />
                    </li>
                    <li>
                      <input
                        type="text"
                        id="PhoneNumber"
                        name="PhoneNumber"
                        v-model="Shippingform.mobnumber"
                        placeholder="Phone Number"
                      />
                    </li>
                    <li>
                      <input
                        type="text"
                        id="Address"
                        name="Address"
                        v-model="Shippingform.address"
                        placeholder="Address"
                      />
                    </li>
                    <li>
                      <input
                        type="text"
                        id="Apartment"
                        name="Apartment"
                        v-model="Shippingform.apartment"
                        placeholder="Apartment, Suite, etc (optional)"
                      />
                    </li>
                    <li>
                      <input
                        type="text"
                        id="State"
                        name="State"
                        v-model="Shippingform.state"
                        placeholder="State"
                      />
                    </li>
                    <li>
                      <input
                        type="text"
                        id="City"
                        name="City"
                        v-model="Shippingform.city"
                        placeholder="City"
                      />
                    </li>
                    <li>
                      <input
                        type="text"
                        id="Country"
                        name="Country"
                        v-model="Shippingform.country"
                        placeholder="Country"
                      />
                    </li>
                    <li>
                      <input
                        type="text"
                        id="ZipCode"
                        v-model="Shippingform.zipcode"
                        name="ZipCode"
                        placeholder="Zip Code"
                      />
                    </li>
                    <li>
                      <label for="Note" class>Thank You Note</label>
                      <textarea
                        rows="2"
                        id="Message"
                        name="Message"
                        placeholder="Write Your Message Here"
                      ></textarea>
                    </li>
                  </ul>
                  <div class="common_btn">
                    <a
                      class="Complete"
                      @click="onSubmitonshipping"
                      @reset="onReset"
                      href="javaScript:void(0)"
                    >
                      <span>Complete</span>
                    </a>
                    <p>
                      Powered by
                      <img src="#" />
                    </p>
                  </div>
                </div>
              </div>
  
              <div id="popup6" class="popup1_mn">
                <div v-if="step === 3">
                <div class="popup_block popup6">
                  <ul class="popup_top popup_new">
                    <div class="pop_inner">
                      <li class="active tick">
                        <span class="circle">
                          <span class="inner_circle"></span>
                        </span>
                        <p>Shipping Details</p>
                      </li>
                      <li class="active tick">
                        <span class="circle">
                          <span class="inner_circle"></span>
                        </span>
                        <p>Complete!</p>
                      </li>
                    </div>
                  </ul>
                  <div class="popup_content">
                    <h1>Complete!</h1>
                    <p>Your present will be on the way soon!</p>
                  </div>
                  <div class="common_btn">
                       <button @click.prevent="prev()">Previous</button>
                    <button @click.prevent="next()">Next</button>
                    <a class="close_btn_new" href="javaScript:void(0)">
                      <span>Close</span>
                    </a>
                    <p>
                      Powered by
                      <img src="#" />
                    </p>
                  </div>
                </div>
              </div>
          </div>
            <!-- </b-modal> -->
          <!-- </div> -->
        </b-row>
      </b-container>
    </template>
  </div>
</template>

    
   

<script>
export default {
  name: "HelloWorld",

  data() {
    return {
      emailto: "",
      nameto: "",
      emailfrom: "",
      namefrom: "",
      msgboxall: "",


      form: {
        email: "",
        name: "",
        yemail: "",
        yname: "",
        msgbox: "",
      },
      Shippingform: {
        fname: "",
        lname: "",
        company: "",
        mobnumber: "",
        address: "",
        apartment: "",
        city: "",
        state: "",
        country: "",
        zipcode: "",
      },

      show: true,
    };
  },
 
  methods: {
    onSubmit(evt) {
      evt.preventDefault();
      //
      (this.emailto = this.form.email),
        (this.nameto = this.form.name),
        (this.emailfrom = this.form.yemail),
        (this.namefrom = this.form.yname),
        (this.msgboxall = this.form.msgbox);
    },
    onSubmitonshipping(evt) {
      evt.preventDefault();
      alert(JSON.stringify(this.Shippingform));
    },
    onReset(evt) {
      evt.preventDefault();
      // Reset our form values
      this.form.email = "";
      this.form.name = "";
      this.form.yemail = "";
      this.form.yname = "";
      this.form.msgbox = "";

      // Trick to reset/clear native browser form validation state
      this.show = false;
      this.$nextTick(() => {
        this.show = true;
      });
    },
      prev() {
      this.step--;
    },
    next() {
      this.step++;
    },
    
  },
};
</script>



<!-- Add "scoped" attribute to limit CSS to this component only -->
   <style scoped src="@/assets/style.css">
</style>

<style>
h3 {
  margin: 40px 0 0;
}
ul {
  list-style-type: none;
  padding: 0;
}
li {
  display: inline-block;
  margin: 0 10px;
}
a {
  color: #42b983;
}
</style>

