<template>
  <AboutUs msg="Welcome to Your Vue.js App"/>
  <DateTemp msg="Welcome to Your Vue.js App"/>
  <OurCustomers msg="Welcome to Your Vue.js App"/>
  <OurServices msg="Welcome to Your Vue.js App"/>
  <BarHmar msg="Welcome to Your Vue.js App"/>

</template>

<script>
import OurCustomers from './components/OurCustomers.vue';
import AboutUs from './components/AboutUs.vue';
import DateTemp from './components/DateTemp.vue';
import OurServices from './components/OurServices.vue';
import BarHmar from './components/NavBar.vue';
export default {
  name: 'App',
  components: {
    OurCustomers,
    AboutUs,
    DateTemp,
    OurServices,
    BarHmar

}
}
</script>

<style>
#app {
  font-family: Avenir, Helvetica, Arial, sans-serif;
  -webkit-font-smoothing: antialiased;
  -moz-osx-font-smoothing: grayscale;
  text-align: center;
  color: #2c3e50;
  margin-top: 60px;
}
</style>
