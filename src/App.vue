<!-- <template>
  <nav>
    <router-link to="/">Home</router-link> |
    <router-link to="/about">About</router-link>
  </nav>
  <router-view/>
</template> -->

<template>
  <nav>
    <NavBarVue></NavBarVue>
    <router-view/>
    <FooterVue></FooterVue>
  </nav>
  <body>

  </body>
</template>

<script>
import NavBarVue from './components/NavBar.vue';
import FooterVue from './components/Footer.vue';


export default {
  components:{
    NavBarVue,
    FooterVue,
  }
}

</script>
<style>
*,
*::after,
*::before {
    margin: 0;
    padding: 0;
    box-sizing: border-box;
}

body {
    text-align: center;
    font-size: 25px;
    font-family:'Oswald', sans-serif;
    background-color: rgb(201, 214, 223);
}





/* #app {
  font-family: Avenir, Helvetica, Arial, sans-serif;
  -webkit-font-smoothing: antialiased;
  -moz-osx-font-smoothing: grayscale;
  text-align: center;
  color: #2c3e50;
}

nav {
  padding: 30px;
}

nav a {
  font-weight: bold;
  color: #2c3e50;
}

nav a.router-link-exact-active {
  color: #42b983;
} */
</style>
