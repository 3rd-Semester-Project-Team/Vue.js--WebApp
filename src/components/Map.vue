<template>

<div class="d-flex flex-row justify-content-center w-100">
    <div class="col-12 col-md-6 col-lg-8">
      <div class="scaleable-wrapper" id="scaleable-wrapper">
        <div class="map-container" id="map-container">
          <div>
	            <i style="font-size: 3.1rem; position: absolute; top: 1%; right:50%" class="bi bi-arrow-down arrows">
              </i>
		          <i style="font-size: 3.1rem; position: absolute; top: 1%; right:45% ;"  class="bi bi-arrow-up arrows">
              </i>
	        </div>
		    </div>
      </div>
    </div>
</div>
	
</template>

<script>
import { onMounted } from '@vue/runtime-core'


export default {
    name: 'parkingmap',
    data () {
        return{
            
        }
    },
    props: {
        parkingSlots: []
    },
    methods: 
	{
        setToOccupied: function () 
		{
             for (let i = 0; i <= this.parkingSlots.length -1;i++)
			 {
                if (this.parkingSlots[i].occupied == true)
				{
                    let slot = document.getElementById(this.parkingSlots[i].parkingId)
                    slot.style.backgroundColor = "#DF0000"
                }
            }
        }
    },
    updated () {
        this.$nextTick(
            this.setToOccupied()
        )
    },
	mounted(){
		var $el = $("#map-container");
var elHeight = $el.outerHeight();
var elWidth = $el.outerWidth();

var $wrapper = $("#scaleable-wrapper");

$wrapper.resizable({
  resize: doResize
});

function doResize(event, ui) {
  
  var scale, origin;
    
  scale = Math.min(
    ui.size.width / elWidth,    
    ui.size.height / elHeight
  );
  
  $el.css({
    transform: "translate(-50%, -50%) " + "scale(" + scale + ")"
  });
  
}

var starterData = { 
  size: {
    width: $wrapper.width(),
    height: $wrapper.height()
  }
}
doResize(null, starterData);


// added code for parking slots

var createTopRight = function () {

	console.log(document.getElementById("scaleable-wrapper"))
  var main = document.getElementById("map-container")
  console.log(main)
  var distH = 0.8;

  for (let i = 0; i <= 8; i++){
    var slot = document.createElement('div')
    slot.style.width = '4%'
    slot.style.height = '14%'
    slot.style.background = '#5CBD4C'
	  slot.setAttribute("id",i+1)
  
    slot.style.position = 'absolute'
    slot.style.top = '1%'
    slot.style.right = distH + i*distH + (i*4) + '%'
    main.append(slot);
  }
}

var createTopLeft = function () {

	console.log(document.getElementById("scaleable-wrapper"))
	//var main =onMounted(document.getElementById("map-container"))
  var main = document.getElementById("map-container")
  console.log(main)
  var distH = 0.8;

  for (let i = 0; i <= 6; i++){
    var slot = document.createElement('div')
    slot.style.width = '4%'
    slot.style.height = '14%'
    slot.style.background = '#5CBD4C'
	slot.setAttribute("id",i+10)
  
    slot.style.position = 'absolute'
    slot.style.top = '1%'
    slot.style.right = 57.6 + i*distH + (i*4) + '%'
    main.append(slot);
  }
}

let createMiddleTop = function () {
  let main = document.getElementById('map-container')
  let distH = 0.8;

  for (let i = 0; i <= 14; i++){
    let slot = document.createElement('div')
    slot.style.width = '4%'
    slot.style.height = '14%'
    slot.style.background = '#5CBD4C'
	slot.setAttribute("id",i+17)
  
    slot.style.position = 'absolute'
    slot.style.top = '34%'
    slot.style.right = distH + i*distH + (i*4) + '%'
    main.append(slot);
  }
}
let createMiddleBottom = function () {
  let main = document.getElementById('map-container')
  let distH = 0.8;

  for (let i = 0; i <= 14; i++){
    let slot = document.createElement('div')
    slot.style.width = '4%'
    slot.style.height = '14%'
    slot.style.background = '#5CBD4C'
	slot.setAttribute("id",i+32)
  
    slot.style.position = 'absolute'
    slot.style.top = '51%'
    slot.style.right = distH + i*distH + (i*4) + '%'
    main.append(slot);
  }
}
let createBottom = function () {
  let main = document.getElementById('map-container')
  let distH = 0.8;

  for (let i = 0; i <= 17; i++){
    let slot = document.createElement('div')


	let special=document.createElement('img')
	special.style.width='80%'
	special.style.height='45%'
	special.style.position='absolute'
	special.style.top='30%'
	special.style.left='10%'
	special.src='wheelchair.png'
	if(i==15 || i==16 || i==17){
		slot.append(special)
	}

    slot.style.width = '4%'
    slot.style.height = '14%'
    slot.style.background = '#5CBD4C'
	slot.setAttribute("id",i+47)
  
    slot.style.position = 'absolute'
    slot.style.top = '85%'
    slot.style.right = distH + i*distH + (i*4) + '%'
    main.append(slot);
  }
}

let createLeft = function () {
  let main = document.getElementById('map-container')
  let distV = 1.5;

  for (let i = 0; i <= 7; i++){
    let slot = document.createElement('div')

    slot.style.width = '7.8%'
    slot.style.height = '7.8%'
    slot.style.background = '#5CBD4C'
	slot.setAttribute("id",i+65)
  
    slot.style.position = 'absolute'
    slot.style.top = 16 + i*distV + (i*7.8) + '%'
    slot.style.left = '1%'
    main.append(slot);
  }
}

let drawParkingSlots = function () {
  createTopLeft()
  createTopRight()
  createMiddleTop()
  createMiddleBottom()
  createBottom()
  createLeft()
}

drawParkingSlots()

	}
	
    
}



</script>

<style>
@import url("https://cdn.jsdelivr.net/npm/bootstrap-icons@1.7.2/font/bootstrap-icons.css");

.map-container {
    width: 950px;
    height: 488px;
    padding: 50px;
    text-align: center;
    background: white;
    position: relative;
    left: 50%;
    top: 50%;
    transform: translate(-50%, -50%);
    transform-origin: center center;
  }
  
  .scaleable-wrapper {
    padding: 10px;
    resize: both;
    position: relative;
    background: #f0f0f0;
    height: 400px;
  }

.occupied {
    background: #DF0000;

}

.fill {
  background:blue;
  width: 100%;
  height: 100%;
}
</style>