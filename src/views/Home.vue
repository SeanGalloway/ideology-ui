<template>
  <div class="home">
    <div id="jumbotron">
      <h1>Ideology</h1>
    </div>
    <button class="main">Propose Idea</button>
    <InfoBox text-key="mission"/>
    <infoBox text-key="values"/>
  </div>
</template>

<script>
// @ is an alias to /src
import InfoBox from '@/components/InfoBox.vue'

export default {
  name: 'Home',
  components: {
    InfoBox
  }
}
</script>

<style scoped>
#jumbotron {
  padding: 100px;
  background-color: #aae6ee;
}

</style>
