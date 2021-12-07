<template>
  <div class="row justify-content-center text-white">
      <div class="d-flex flex-column box free m-3 justify-content-center">
          <h1>{{getAvailable()}}</h1>
          <h4>Available</h4>
      </div>
        <div class="d-flex flex-column box occupied m-3 justify-content-center">
          <h1>{{getOccupied()}}</h1>
          <h4>Occupied</h4>
      </div>
  </div>
</template>

<script>
export default {
    name: 'availability',
    data () {
        return {

        }
    },
    props: {
        parkingSlots: []
    },
    methods: {
        getAvailable: function (){
            // let count = 0;
            // for (let i = 0; i <= this.parkingSlots.length -1;i++){
            //     if (this.parkingSlots[i].occupied == false){
            //         count++
            //     }
            // }
            // console.log(count)
            // return count;
            return 72 - this.getOccupied()
        },
        getOccupied: function () {
            let count = 0;
                        for (let i = 0; i <= this.parkingSlots.length -1;i++){
                if (this.parkingSlots[i].occupied == true){
                    count++
                }
            }
            console.log(count)
            return count;
        }
    }
}
</script>

<style>
.box {
    width: 150px;
    height: 150px;
    border-radius: 15px;
    text-align: center;
}

.free {
    background: #5CBD4C;
}

.occupied {
    background: #DF0000;
}

h1 {
    font-size: 5rem;
    margin: 0;
}
</style>