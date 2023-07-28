<script setup>
import { ref,reactive } from 'vue';
// const location = ref('Dhaka');
const location = reactive({
    name:'Dhaka',
    weather:'sunny'
});

function buttonClick(e,f){
    // alert('Click '+e);
    location.name = e;
    location.weather = f;
}
</script>


<template>

<hr>
<h4 class="text-center"> Event + Reactive </h4>
<hr>
 
 
    <button class="btn btn-primary mr-4" @click="buttonClick('Dhaka','rainny')"> Dhaka </button>
    <button class="btn btn-primary mr-4" @click="buttonClick('Rajshahi','thunder')"> Rajshahi </button>
 
 
<h3 class="mt-4"> Current location is {{ location.name }} - weather : {{ location.weather }}</h3>
    </template>