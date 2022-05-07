<template>
  <div class="flex flex-col flex-center">
    Register
    <LabeledInput label="Email" v-model="email"/>
    <LabeledInput label="Phone" v-model="phone"/>
    <LabeledInput label="Your Name" v-model="name"/>
    <LabeledInput label="Password" v-model="password"/>
    <LabeledInput label="Confirm" v-model="confirmPassword"/>
    <div class="error" v-if="!passwordsMatch">Passwords do not match</div>
    <button class="main" v-on:click="submit">Submit</button>
  </div>
</template>

<script>
import LabeledInput from "@/components/LabeledInput.vue";
import axios from 'axios';
export default {
  name: 'Register',
  components: {
    LabeledInput
  },
  data () {
    return {
      email: "",
      phone: "",
      name: "",
      password: "",
      confirmPassword: ""
    }
  },
  computed: {
    passwordsMatch: function() {
      return this.password === this.confirmPassword
    }
  },
  methods: {
    submit () {

      if (this.passwordsMatch) {
        axios.post("auth/register", {
          email: this.email,
          phone: this.phone,
          name: this.name,
          password: this.password
        }).then(response => {
          console.log(response.data);
        }).catch(err => {
          console.log(err);
        });
      }
    }
  }

}
</script>