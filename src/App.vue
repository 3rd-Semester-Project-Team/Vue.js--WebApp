<template>
  <img alt="Vue logo" src="./assets/logo.png">
  <HelloWorld msg="Welcome to Your Vue.js App"/>
  <mymap :parking="dataList"/>
</template>

<script>
import HelloWorld from './components/HelloWorld.vue'
import mymap from './components/Map.vue'

export default {
  name: 'App',
  components: {
    HelloWorld, mymap
  },
  data (){ 
    return {
    dataList: [1,2,3], // fake data for the example
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
    }
  }, 
  created () {
    // is called when this component is created
    this.getAllParkingSlots()
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
