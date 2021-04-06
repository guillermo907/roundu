<template>
  <Navbar />
  <router-view></router-view>
  <div v-if='locationReady'>
    <LocationCard :adress='address'/>
  </div>
  <div v-else>
    Cargando latitud ...
  </div>
</template>

<script>
import Navbar from './components/Navbar';
import LocationCard from './components/LocationCard';

import Axios from 'axios';

export default {
  name: 'App',
  data(){
    return {
      location: {},
      address: {}
    }
  },
  computed:{
    locationReady (){
      return this.location.latitude ? true : false;
    }
  },
  components: {
    Navbar,
    LocationCard
  },
  created(){
    navigator.geolocation.watchPosition(result =>{
      this.location = result.coords;
      this.getAdress();
    }, console.log('error de geolocalizacion'));
  },
  methods: {
    getAdress(){
      Axios.get(`https://nominatim.openstreetmap.org/reverse?format=json&lat=${this.location.latitude}&lon=${this.location.longitude}&zoom=18&addressdetails=1`)
      .then(res => {
              console.log(res.data);
              this.address = res.data.address;
            })
    }
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
  margin-top: 20px;
}
p{
  text-align: left;
}
</style>
