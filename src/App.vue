<template>
  <div id="nav">
    <!-- router link are anchor -->
    <router-link to="/">Home</router-link> |
    <router-link to="/about">About</router-link> |
    <router-link to="/blog">Blog</router-link>
  </div>
  <!-- 
    Allows dynamic content changes 
    This is managed by ./router/index.js
  -->
  <router-view/>
</template>

<style>
#app {
  font-family: Avenir, Helvetica, Arial, sans-serif;
  -webkit-font-smoothing: antialiased;
  -moz-osx-font-smoothing: grayscale;
  text-align: center;
  color: #2c3e50;
}

#nav {
  padding: 30px;
}

#nav a {
  font-weight: bold;
  color: #2c3e50;
}

/* Choose the color in which the chosen route is painted */
#nav a.router-link-exact-active {
  color: #42b983;
}
</style>
