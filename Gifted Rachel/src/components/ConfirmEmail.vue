<template>
    <div>
        <div class="container my-2">
        <b-col md="8 mx-auto">
        <b-card>
        <h4>Sender name</h4>
        <h4>The Email With Your Gift is On the way Recievers </h4>
        <h4>You Made Recievers Day</h4>
        </b-card>
        </b-col>
        </div>
        
    </div>
</template>

<script>
export default {
  name: "ConfirmEmail",
  props: {
    msg: String,
  },
  data() {
    return {
            }
         }
}
  </script>