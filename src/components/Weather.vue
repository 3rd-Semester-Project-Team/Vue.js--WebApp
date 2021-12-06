<template>
<div class="container text-white weather bg-secondary">
  <div class="d-flex flex-row w-100 justify-content-right">
      <div class="col text-right">
          <p>{{date()}}</p>
           <p v-if="weather != null">{{weather.main.temp}} &#176;C {{weather.weather[0].main}}  </p>

      </div>
      <div class="col text-right">
          <img v-if="weather != null" v-bind:src="'https://openweathermap.org/img/w/' + weather.weather[0].icon + '.png'">
          </div>
  </div>
</div>
</template>

<script>
export default {
    name: 'weather',
    data () {
        return {
            weather : null 

            
        }

    },
    methods: {
        date: function () {
            let date = new Date()
            return date.toLocaleDateString()
        },
        getWeather: function() {
            axios.get("https://api.openweathermap.org/data/2.5/weather?q=Roskilde&appid=10edbc177a0e566ad00fac132ccb8e0d&units=metric")
           .then(response=>{
        console.log(response.status)
        this.weather = response.data
        console.log(this.weather)
      })
      .catch(function(error){
        console.log(error)
      })
        }
    },
     created () {
    // is called when this component is created
    this.getWeather()
  }
}
</script>

<style>
.weather {
    width: 300px;
    max-width: 300px;
}
</style>