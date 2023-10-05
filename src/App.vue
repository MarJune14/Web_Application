

<script setup>
import { ref } from 'vue'



const color = ref ('');
const height = ref ('0');
const width = ref ('0');
const radius = ref ('')

</script>
<template>
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

        <div class="txt" ><p> Color: {{ color }} Height: {{ height}} Width: {{width}} Radius: {{ radius }}</p>
        </div>
        <div class="box">
        </div>
    </div>
</div>
</form>

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
    left: 320px;
    top: 42px;
}
.input-width {
    position:absolute;
    left:320px;
    top: 83px
}
.input-radius {
    position: absolute;
    left: 320px;
    top: 123px;
}


</style>