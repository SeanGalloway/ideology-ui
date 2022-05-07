<template>
  <div class="flex flex-col flex-center">
    Register
    <LabeledInput label="Email" v-model="email"/>
    <LabeledInput label="Password" v-model="password"/>
    <button class="main" v-on:click="submit">Submit</button>
  </div>
</template>

<script>
import LabeledInput from "@/components/LabeledInput.vue";
import axios from 'axios';

export default {
  name: 'Login',
  components: {
    LabeledInput
  },
  data () {
    return {
      email: "",
      password: ""
    }
  },
  methods: {
    submit () {
        axios.post("auth/login", {
          email: this.email,
          password: this.password
        }).then(response => {
          console.log(response.data);
        }).catch(err => {
          console.log(err);
        });
    }
  }

}
</script>