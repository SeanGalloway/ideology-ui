<template>
  <div id="app">
    <div id="nav">
<!--      <router-link id="logo-link" to="/"><img id="logo" src="./assets/ideology_logo.svg" alt="ideology logo"/></router-link>-->
      <router-link to="/">Propose Idea</router-link> |
      <router-link to="/about">About</router-link> |
      <router-link to="/login">Login</router-link> |
      <router-link to="/register">Register</router-link>
    </div>
    <router-view/>
  </div>
</template>

<style>
#app {
  font-family: Avenir, sans-serif;
  -webkit-font-smoothing: antialiased;
  -moz-osx-font-smoothing: grayscale;
  text-align: center;
  color: #2c3e50;
}

#nav {
  padding: 10px;
  text-align: right;
  box-shadow: 0 1px 5px grey;
}

#logo-link {
  float: left;
}

#logo {
  padding: .2em;
  height: 2.5em;
}

#nav a {
  font-weight: bold;
  text-decoration: none;
  color: #FFBA3E;
}
</style>
