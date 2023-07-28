<script setup>
import { ref,reactive } from 'vue';

const bigImage = ref("https://images.unsplash.com/photo-1631603090989-93f9ef6f9d80?ixlib=rb-4.0.3&ixid=M3wxMjA3fDB8MHxzZWFyY2h8Nnx8Y3J5cHRvfGVufDB8fDB8fHww&auto=format&fit=crop&w=500&q=60")

const images = reactive([
        {id:1,imageSrc:"https://images.unsplash.com/photo-1631603090989-93f9ef6f9d80?ixlib=rb-4.0.3&ixid=M3wxMjA3fDB8MHxzZWFyY2h8Nnx8Y3J5cHRvfGVufDB8fDB8fHww&auto=format&fit=crop&w=500&q=60"},
        {id:2,imageSrc:"https://images.unsplash.com/photo-1634704784915-aacf363b021f?ixlib=rb-4.0.3&ixid=M3wxMjA3fDB8MHxzZWFyY2h8OXx8Y3J5cHRvfGVufDB8fDB8fHww&auto=format&fit=crop&w=500&q=60"},
        {id:3,imageSrc:"https://images.unsplash.com/photo-1622630998477-20aa696ecb05?ixlib=rb-4.0.3&ixid=M3wxMjA3fDB8MHxzZWFyY2h8MTF8fGNyeXB0b3xlbnwwfHwwfHx8MA%3D%3D&auto=format&fit=crop&w=500&q=60"},
        {id:4,imageSrc:"https://images.unsplash.com/photo-1629339942248-45d4b10c8c2f?ixlib=rb-4.0.3&ixid=M3wxMjA3fDB8MHxzZWFyY2h8MTV8fGNyeXB0b3xlbnwwfHwwfHx8MA%3D%3D&auto=format&fit=crop&w=500&q=60"},
])

function setImage(image){
    bigImage.value = image.imageSrc;
}
 
</script>


<template>



<hr>
<h4 class="text-center"> Creating an Image Slider </h4>
<hr>
 
 

<div class="row">
    <div class="col-md-3"></div>
    <div class="col-md-6">
    <div class="col-md-12">

        <div class="col-md-12">
        <div class="row">
            <div class="col-md-3" v-for="image in images" :key="image.id">
                <img @click="setImage(image)" :src="image.imageSrc" style="width: 100px;cursor: pointer;">
            </div>
            
            </div>
        </div>


        <div class="col-md-12">
                <img class="mt-4" :src="bigImage">
            </div>

            
            </div>




    </div>


    
</div>
    </template>