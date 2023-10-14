

<script setup>
import { ref } from 'vue'



const color = ref ('');
const height = ref ('');
const width = ref ('');
const radius = ref ('')

</script>
<template>

<div class="container mt-3">
  <h3>COSTUMIZE YOUR BOX</h3>
  
  
  <button type="button" class="btn btn-primary" data-bs-toggle="modal" data-bs-target="#myModal">
    Click to Open
  </button>
</div>


<div class="modal fade" id="myModal">
  <div class="modal-dialog">
    <div class="modal-content">

      <!-- Modal Header -->
      <div class="modal-header">
        <h4 class="modal-title">Costumize your BOX</h4>
        <button type="button" class="btn-close" data-bs-dismiss="modal"></button>
      </div>

      <!-- Modal body -->
      <div class="modal-body">
        <form>
<div class="container">
    <div class="vertical-container">
        <p>COLOR: <input type="text" v-model="color" :disabled="isDisabled"/></p>
       <p> HEIGHT: <select v-model="height">
            <option value="" disabled selected>Choose your option</option>
            <option value="100px">100px</option>    
            <option value="200px">200px</option>
            <option value="300px">300px</option>
            <option value="400px">400px</option>
            <option value="500px">500px</option>
            </select>
            
                
    
                <div class="input-height">
                    <input type="text" v-model="height"/>
                </div> </p>

        <p>WIDTH: <select v-model="width ">
            <option value="" disabled selected>Choose your option</option>
            <option value="100px">100px</option>    
            <option value="200px">200px</option>
            <option value="300px">300px</option>
            <option value="400px">400px</option>
            <option value="500px">500px</option>
            
                </select>
    
                <div class="input-width">
                    <input type="text" v-model="width"/>
                </div></p>

        <p>RADIUS: <select v-model="radius" >
            <option value="15px">15px</option>
            <option value="25px">25px</option>
            <option value="50px">50px</option>
            <option value="15px 50px 30px 5px">15px 50px 30px 5px</option>
            <option value="15px 50px 30px">15px 50px 30px</option>
            <option value="15px 50px">15px 50px</option>
                </select>

                <div class="input-radius">
                    <input type="text" v-model="radius"/>
                </div></p>

        <div class="txt" >
        <p> Color: {{ color }} </p>
        <p> Height: {{ height}} </p>
        <p> Width: {{ width }} </p>
        <p> Radius: {{ radius }} </p>
        </div>
        <div class="box">
        </div>
    </div>
</div>
</form>
      </div>

      <!-- Modal footer -->
      <div class="modal-footer">
        <button type="button" class="btn btn-danger" data-bs-dismiss="modal">Close</button>
      </div>

    </div>
  </div>
</div>


</template>

<style>

.box {
    background-color: v-bind(color);
    height: v-bind(height);
    width: v-bind(width);
    border-radius: v-bind(radius);
    position:center;
    left:500px;
}
.txt {
    font-style: italic;
    font-weight: bold;
}



.input-height {
    position:absolute;
    left: 300px;
    top: 60px;
}
.input-width {
    position:absolute;
    left:300px;
    top: 100px
}
.input-radius {
    position: absolute;
    left: 300px;
    top: 140px;
}


</style>