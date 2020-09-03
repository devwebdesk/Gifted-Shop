<template>
  <div class="hello">
    <template>
      <b-container>
        <b-row>
          <b-col md="8 mx-auto">
            <!-- <div>
  <b-button v-b-modal.modal-center>Click Here</b-button>

  <b-modal id="modal-center" centered title=""> -->
  
 
            <b-card>
              <form @submit="onSubmitonshipping"  v-if="show">
                 <div v-if="step === 1">
                <b-row>
                  <b-col md="12">
                    <h4>Shipping Details</h4>
                    <br />
                  </b-col>

                  <b-col md="6">
                    <b-form-group id="input-group-5">
                      <b-form-input
                        id="input-5"
                        v-model="Shippingform.fname"
                        required
                        placeholder="First Name"
                      ></b-form-input>
                    </b-form-group>

                    <b-form-group id="input-group-6">
                      <b-form-input
                        id="input-6"
                        v-model="Shippingform.company"
                        required
                        placeholder="Company"
                      ></b-form-input>
                    </b-form-group>

                    <b-form-group id="input-group-7">
                      <b-form-input
                        id="input-7"
                        v-model="Shippingform.address"
                        required
                        placeholder="Address"
                      ></b-form-input>
                    </b-form-group>

                    <b-form-group id="input-group-8">
                      <b-form-input
                        id="input-8"
                        v-model="Shippingform.city"
                        required
                        placeholder="City"
                      ></b-form-input>
                    </b-form-group>

                    <b-form-group id="input-group-9">
                      <b-form-input
                        id="input-9"
                        v-model="Shippingform.country"
                        required
                        placeholder="Country"
                      ></b-form-input>
                    </b-form-group>
                  </b-col>
                  <b-col md="6">
                    <b-form-group id="input-group-10">
                      <b-form-input
                        id="input-10"
                        v-model="Shippingform.lname"
                        required
                        placeholder="Last Name"
                      ></b-form-input>
                    </b-form-group>

                    <b-form-group id="input-group-11">
                      <b-form-input
                        id="input-11"
                        v-model="Shippingform.mobnumber"
                        required
                        placeholder="Phone Number"
                      ></b-form-input>
                    </b-form-group>

                    <b-form-group id="input-group-12">
                      <b-form-input
                        id="input-12"
                        v-model="Shippingform.apartment"
                        required
                        placeholder="Apartment, Suit, Etc"
                      ></b-form-input>
                    </b-form-group>

                    <b-form-group id="input-group-13">
                      <b-form-input
                        id="input-13"
                        v-model="Shippingform.state"
                        required
                        placeholder="State"
                      ></b-form-input>
                    </b-form-group>

                    <b-form-group id="input-group-14">
                      <b-form-input
                        id="input-14"
                        v-model="Shippingform.zipcode"
                        required
                        placeholder="Zip Code"
                      ></b-form-input>
                    </b-form-group>
                  </b-col>
                  <b-button type="submit" variant="primary">Submit</b-button>
                   <button @click.prevent="next()">Next</button>
                </b-row>
                 </div>
               
                
                <div v-if="step === 2">
                <b-card class="mt-3" header="Complate Data">
      
              <b-row>
                <b-col md="12">
                  <h5>Complate!!!!</h5>
                  <h6>Your Present will be on the way soon!!</h6>
                </b-col>
               
              </b-row>
            </b-card>
             <br>
                <br>
             <button @click.prevent="prev()">Previous</button>
    <button @click.prevent="next()">Next</button>
                </div>
               
              </form>
            </b-card>
             <!-- </b-modal>
</div> -->

          
             
          </b-col>
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
      step:1,
      emailto: "",
      nameto: "",
      emailfrom: "",
      namefrom: "",
      msgboxall: "",


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
      alert(JSON.stringify(this.Shippingform));
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

