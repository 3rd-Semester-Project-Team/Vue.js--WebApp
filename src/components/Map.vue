<template>
    <div class="main-container">	
   
    <!-- Top right -->
		<canvas class="slot" id="1" width="40" height="70" style="top: 5px; right: 5px;"></canvas>
    		<canvas class="slot" id="2" width="40" height="70" style="top: 5px; right: 47px;"></canvas>
		<canvas class="slot" id="3" width="40" height="70" style="top: 5px; right: 89px;"></canvas>
		<canvas class="slot" id="4" width="40" height="70" style="top: 5px; right: 131px;"></canvas>
		<canvas class="slot" id="5" width="40" height="70" style="top: 5px; right: 173px;"></canvas>
		<canvas class="slot" id="6" width="40" height="70" style="top: 5px; right: 215px;"></canvas>
    		<canvas class="slot" id="7" width="40" height="70" style="top: 5px; right: 257px;"></canvas>
		<canvas class="slot" id="8" width="40" height="70" style="top: 5px; right: 299px;"></canvas>
		<canvas class="slot" id="9" width="40" height="70" style="top: 5px; right: 341px;"></canvas>
 
  <!-- Top left -->
		<canvas class="slot" id="10" style="top: 5px; left: 89px;"></canvas>
		<canvas class="slot" id="11" style="top: 5px; left: 131px;"></canvas>
  		<canvas class="slot" id="12" style="top: 5px; left: 173px;"></canvas>
  		<canvas class="slot" id="13" style="top: 5px; left: 215px;"></canvas>
  		<canvas class="slot" id="14" style="top: 5px; left: 257px;"></canvas>
  		<canvas class="slot" id="15" style="top: 5px; left: 299px;"></canvas>
		<canvas class="slot" id="16" style="top: 5px; left: 341px;"></canvas>
  
  <!-- Middle 1 -->
	<canvas id="72" class="slot" width="40" height="70" style="top: 156px; right: 5px;"></canvas> 
	<canvas id="71" class="slot" width="40" height="70" style="top: 156px; right: 47px;"></canvas> 
	<canvas id="70" class="slot" width="40" height="70" style="top: 156px; right: 89px;"></canvas> 
	<canvas id="69" class="slot" width="40" height="70" style="top: 156px; right: 131px;"></canvas> 
	<canvas id="68" class="slot" width="40" height="70" style="top: 156px; right: 173px;"></canvas> 
	<canvas id="67" class="slot" width="40" height="70" style="top: 156px; right: 215px;"></canvas> 
	<canvas id="66" class="slot" width="40" height="70" style="top: 156px; right: 257px;"></canvas> 
	<canvas id="65" class="slot" width="40" height="70" style="top: 156px; right: 299px;"></canvas> 	
	<canvas id="64" class="slot" width="40" height="70" style="top: 156px; right: 341px;"></canvas> 
	<canvas id="63" class="slot" width="40" height="70" style="top: 156px; right: 383px;"></canvas> 
	<canvas id="62" class="slot" width="40" height="70" style="top: 156px; right: 425px;"></canvas> 
	<canvas id="61" class="slot" width="40" height="70" style="top: 156px; right: 467px;"></canvas> 
	<canvas id="60" class="slot" width="40" height="70" style="top: 156px; right: 509px;"></canvas> 
	<canvas id="59" class="slot" width="40" height="70" style="top: 156px; right: 551px;"></canvas> 
	<canvas id="58" class="slot" width="40" height="70" style="top: 156px; right: 593px;"></canvas>

  <!-- Middle 2 -->

	<canvas id="43" class="slot" width="40" height="70" style="top: 228px; right: 5px;"></canvas> 
	<canvas id="44" class="slot" width="40" height="70" style="top: 228px; right: 47px;"></canvas> 
	<canvas id="45" class="slot" width="40" height="70" style="top: 228px; right: 89px;"></canvas> 
	<canvas id="46" class="slot" width="40" height="70" style="top: 228px; right: 131px;"></canvas> 
	<canvas id="47" class="slot" width="40" height="70" style="top: 228px; right: 173px;"></canvas> 
	<canvas id="48" class="slot" width="40" height="70" style="top: 228px; right: 215px;"></canvas> 
	<canvas id="49" class="slot" width="40" height="70" style="top: 228px; right: 257px;"></canvas> 
	<canvas id="50" class="slot" width="40" height="70" style="top: 228px; right: 299px;"></canvas> 
	<canvas id="51" class="slot" width="40" height="70" style="top: 228px; right: 341px;"></canvas> 
	<canvas id="52" class="slot" width="40" height="70" style="top: 228px; right: 383px;"></canvas> 
	<canvas id="53" class="slot" width="40" height="70" style="top: 228px; right: 425px;"></canvas> 
	<canvas id="54" class="slot" width="40" height="70" style="top: 228px; right: 467px;"></canvas> 
	<canvas id="55" class="slot" width="40" height="70" style="top: 228px; right: 509px;"></canvas> 
	<canvas id="56" class="slot" width="40" height="70" style="top: 228px; right: 551px;"></canvas> 
	<canvas id="57" class="slot" width="40" height="70" style="top: 228px; right: 593px;"></canvas> 
    <!-- Left row -->
  <canvas id="17" class="slot-h" style="top: 72px; left: 5px;"></canvas>
  <canvas id="18" class="slot-h" style="top: 114px; left: 5px;"></canvas>
  <canvas id="19" class="slot-h" style="top: 156px; left: 5px;"></canvas>
  <canvas id="20" class="slot-h" style="top: 198px; left: 5px;"></canvas>
  <canvas id="21" class="slot-h" style="top: 240px; left: 5px;"></canvas>
  <canvas id="22" class="slot-h" style="top: 282px; left: 5px;"></canvas>
  <canvas id="23" class="slot-h" style="top: 324px; left: 5px;"></canvas>
  <canvas id="24" class="slot-h" style="top: 366px; left: 5px;"></canvas>
  

    <!-- Bottom row -->
	<canvas id="42" class="slot" width="40" height="70" style="top: 370px; right: 5px;"></canvas>
	<canvas id="41" class="slot" width="40" height="70" style="top: 370px; right: 47px;"></canvas>
 	<canvas id="40" class="slot" width="40" height="70" style="top: 370px; right: 89px;"></canvas> 
	<canvas id="39" class="slot" width="40" height="70" style="top: 370px; right: 131px;"></canvas> 
	<canvas id="38" class="slot" width="40" height="70" style="top: 370px; right: 173px;"></canvas> 
	<canvas id="37" class="slot" width="40" height="70" style="top: 370px; right: 215px;"></canvas> 
	<canvas id="36" class="slot" width="40" height="70" style="top: 370px; right: 257px;"></canvas> 
	<canvas id="35" class="slot" width="40" height="70" style="top: 370px; right: 299px;"></canvas> 
	<canvas id="34" class="slot" width="40" height="70" style="top: 370px; right: 341px;"></canvas> 
	<canvas id="33" class="slot" width="40" height="70" style="top: 370px; right: 383px;"></canvas> 
	<canvas id="32" class="slot" width="40" height="70" style="top: 370px; right: 425px;"></canvas> 
	<canvas id="31" class="slot" width="40" height="70" style="top: 370px; right: 467px;"></canvas> 
	<canvas id="30" class="slot" width="40" height="70" style="top: 370px; right: 509px;"></canvas> 
	<canvas id="29" class="slot" width="40" height="70" style="top: 370px; right: 551px;"></canvas> 
	<canvas id="28" class="slot" width="40" height="70" style="top: 370px; right: 593px;"></canvas> 
	<canvas id="27" class="slot" width="40" height="70" style="top: 370px; right: 635px;"></canvas> 
	<canvas id="26" class="slot" width="40" height="70" style="top: 370px; right: 677px;"></canvas> 
	<canvas id="25" class="slot" width="40" height="70" style="top: 370px; right: 719px;"></canvas>


	</div>
</template>

<script>
export default {
    name: 'parkingmap',
    data () {
        return{
            
        }
    },
    props: {
        parkingSlots: []
    },
    methods: {
        setToOccupied: function () {
             for (let i = 0; i <= this.parkingSlots.length -1;i++){
                if (this.parkingSlots[i].occupied == true){
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
    }
    
}


</script>

<style>

.main-container {
  border: 1px solid black;
  width: 850px;
  height:448px;
  position:relative;
  background: lightgrey;
}
.slot {
  position: absolute;
  box-sizing: border-box;
  width: 40px;
  height: 70px;
  border:0.1px solid;
  background: #5CBD4C;
}

.slot-h {
  position: absolute;
  box-sizing: border-box;
  width: 70px;
  height: 40px;
  border:0.1px solid;
  background: #5CBD4C;
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