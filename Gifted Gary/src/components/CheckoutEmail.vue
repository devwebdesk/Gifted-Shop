<template>
    <div>
        <div class="container my-2">
        <b-col md="8 mx-auto">
        <b-card>
        
        <h4>Hii {{btntext}} name</h4>
        <h4>Reciever name accept your gift from 1$Shop</h4>
        <h4>Sender Notes:Message</h4>

        <br>
        <h5>Reciver Shipping Details</h5>
        <h6>Phone Number:</h6>
        <h6>Company:</h6>
        <h6>Address:</h6>
        <h6>Zipcode:</h6>
        </b-card>
        </b-col>
        </div>
        
    </div>
</template>

<script>
export default {
  name: "CheckoutEmail",
  props: {
    btntext: String
  },
  data() {
    return {
            }
         }
}
  </script>