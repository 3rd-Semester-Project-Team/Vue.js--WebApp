<template>
  <nav class="navbar navbar-expand-sm navbar-dark bg-dark">
  <a class="navbar-brand" href="#"><span class="capital">Z</span>EALAND <span class="capital">P</span>ARKING</a>
  <button class="navbar-toggler" type="button" data-toggle="collapse" data-target="#navbarSupportedContent" aria-controls="navbarSupportedContent" aria-expanded="false" aria-label="Toggle navigation">
    <span class="navbar-toggler-icon"></span>
  </button>

  <div class="collapse navbar-collapse" id="navbarSupportedContent">
    <ul class="navbar-nav mr-auto ">
      <li class="nav-item">
        <a class="nav-link" href="#">Home</a>
      </li>
      <li class="nav-item">
        <a class="nav-link" href="#">About</a>
      </li>
      <li class="nav-item dropdown">

      </li>
      <li class="nav-item">
      </li>
    </ul>
    <weather/>
  </div>
</nav>
  
  <availability :parkingSlots="this.parkingSlots"/>

<div class="row justify-content-center">
    <parkingmap :parkingSlots="parkingSlots"/>
  </div>
  <!-- <parkingmap :parkingSlots="parkingSlots"/> -->

  
</template>

<script>
import parkingmap from './components/Map.vue'
import availability from './components/Availability.vue'
import weather from './components/Weather.vue'

export default {
  name: 'App',
  components: {
    parkingmap, availability, weather
  },
  data (){ 
    return {
    //dataList: [1,2,3], // fake data for the example
    parkingSlots: [],
    apiUrl: 'http://localhost:41911/api/Parkings'
    }
  },
  methods: {
    getAllParkingSlots: function () {
      axios.get(this.apiUrl)
      .then(response=>{
        console.log(response.status)
        this.parkingSlots = response.data
        console.log(this.parkingSlots)
      })
      .catch(function(error){
        console.log(error)
      })
    },
    getCurrentStatus: function () {
      axios.get(this.apiUrl + '/latest')
      .then(response=>{
        console.log(response.status)
        this.parkingSlots = response.data
        console.log(this.parkingSlots)
      })
      .catch(function(error){
        console.log(error)
      })
    },
  }, 
  created () {
    // is called when this component is created
    this.getCurrentStatus()
  }  
    
  }

</script>

<style>
#app {
  font-family: Roboto, Helvetica, Arial, sans-serif;
  -webkit-font-smoothing: antialiased;
  -moz-osx-font-smoothing: grayscale;
}

.navbar-brand {
  font-weight: 700;
  font-size: 1.5rem;
  padding: 0;
}

.capital {
  font-size: 2rem;  
}

.nav-link {
  color: white !important;
  font-size: 1.25rem
}
</style>
