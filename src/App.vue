<script setup>
import { ref } from 'vue'

const color = ref ('');
const height = ref ('0');
const width = ref ('0');
const radius = ref ('');

</script>
<template>
<form>
<p>COLOR: <input type="text" v-model.lazy="color" /></p>
HEIGHT: <select v-model.lazy="height">
    <option value="0" >0</option>
    <option value="100px">100px</option>    
    <option value="200px">200px</option>
    <option value="300px">300px</option>
    <option value="400px">400px</option>
    <option value="500px">500px</option>
    </select>
    
    <input type="text" v-model.lazy="height"/>

<p>WIDTH: <select v-model.lazy="width ">
    <option value="0" >0</option>
    <option value="100px">100px</option>    
    <option value="200px">200px</option>
    <option value="300px">300px</option>
    <option value="400px">400px</option>
    <option value="500px">500px</option>
    </select>
    

    <input type="text" v-model.lazy="width"/>
    </p>

RADIUS: <select v-model.lazy="radius" >
        <option value="15px">15px</option>
        <option value="25px">25px</option>
        <option value="50px">50px</option>
        <option value="15px 50px 30px 5px">15px 50px 30px 5px</option>
        <option value="15px 50px 30px">15px 50px 30px</option>
        <option value="15px 50px">15px 50px</option>
        </select>

        <input type="text" v-model.lazy="radius"/>

<div class="txt" ><p> Color: {{ color }} Height: {{ height}} Width: {{width}} Radius: {{ radius }}</p>

</div>
<div class="box"></div>

</form>

</template>

<style>

.box {
    background-color: v-bind(color);
    height: v-bind(height);
    width: v-bind(width);
    border-radius: v-bind(radius)   
}
.txt {
    font-style: italic;
    font-weight: bold;
}

</style>