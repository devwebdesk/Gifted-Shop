

<template>
  <div class="hello">
    <template>
      <b-container>
        <b-row>
         
          <div v-if="step === 1">
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
                    <span @click.prevent="next()" @click="onSubmit" @reset="onReset">Complete</span>
                  </a>
                  <p>
                    Powered by
                    <img src="#" />
                  </p>
                </div>
              </div>
            </div>
          </div>

          <div v-if="step === 2">
            <div id="popup6" class="popup1_mn">
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
                  <a class="close_btn_new" href="javaScript:void(0)">
                    <span @click.prevent="next()">Close</span>
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
      step: 1,
      emailto: "",
      nameto: "",
      emailfrom: "",
      namefrom: "",
      msgboxall: "",
      firstname: "",
      lastname: "",
      comp: "",
      mobile: "",
      add: "",
      apart: "",
      cityname: "",
      statename: "",
      contname: "",
      zip: "",

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
    onSubmitonshipping(evt) {
      evt.preventDefault();
      // alert(JSON.stringify(this.Shippingform));
      (this.firstname = this.Shippingform.fname),
        (this.lastname = this.Shippingform.lname),
        (this.comp = this.Shippingform.company),
        (this.mobile = this.Shippingform.mobnumber),
        (this.add = this.Shippingform.address),
        (this.apart = this.Shippingform.fnamapartmente),
        (this.cityname = this.Shippingform.city),
        (this.statename = this.Shippingform.state),
        (this.contname = this.Shippingform.country),
        (this.zip = this.Shippingform.zipcode);
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

