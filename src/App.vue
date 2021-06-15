<template>
  <div id="app">
    <img src="./assets/logo.png">
    <Navbar></Navbar>
    <router-view/>
  </div>

</template>

<script>
import Contact from "./components/Contact";
import About from "./components/About";
import Navbar from "./components/Navbar";

export default {
  name: 'App',
  components: {Navbar, Contact, About},
  data(){
    return {
    }
  },
}
</script>


<style>
#app {
  font-family: 'Avenir', Helvetica, Arial, sans-serif;
  -webkit-font-smoothing: antialiased;
  -moz-osx-font-smoothing: grayscale;
  text-align: center;
  color: #2c3e50;
  margin-top: 60px;
}
</style>
