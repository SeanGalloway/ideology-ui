<template>
  <div>
    {{info}}
  </div>
</template>


<script>
import axios from 'axios';

export default {
  name: 'InfoBox',
  props: {
    textKey: String
  },
  data () {
    return {
      info: null,
      loading: true,
      errored: false
    }
  },
  mounted () {
    axios.get("text/" + this.textKey)
      .then(response => {
        this.info = response.data;
      });
  }
}
</script>


<style scoped>


div {
  border: 1px #707070;
  border-radius: 10px;
}
</style>
