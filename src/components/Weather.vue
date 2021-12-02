<template>
<div class="container text-white weather bg-secondary">
  <div class="d-flex flex-row w-100 justify-content-right">
      <div class="col text-right">
          <p>{{date()}}</p>
      </div>
      <div class="col text-right">
          image
          </div>
  </div>
</div>
</template>

<script>
export default {
    name: 'weather',
    data () {

    },
    methods: {
        date: function () {
            let date = new Date()
            return date.toLocaleDateString()
        },
        getWeather: function() {
            axios.get()
        }
    }
}
</script>

<style>
.weather {
    width: 300px;
    max-width: 300px;
}
</style>