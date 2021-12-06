<template>
<!-- <div class="container text-white justify-content-right weather"> -->
  <div class="d-flex flex-row w-100 justify-content-right weather text-white">
      <div class="d-flex flex-column text-right bg-secondary justify-content-center weather-text">
          <div>{{date()}}</div>
           <div v-if="weather != null">{{weather.main.temp}} &#176;C <br> {{weather.weather[0].description}}  </div>
      </div>
      <div class="col text-right icon">
          <img v-if="weather != null" v-bind:src="'https://openweathermap.org/img/w/' + weather.weather[0].icon + '.png'">
          </div>
  </div>
<!-- </div> -->
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
    width: fit-content;
    max-width: 300px;
}

.weather-text {
  padding: 8px;
}

.icon {
  max-width: 91px;
}

.icon img {
  width: 90px;
  height: 90px;
}
</style>