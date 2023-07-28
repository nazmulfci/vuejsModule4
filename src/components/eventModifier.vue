<script setup>
import { ref,reactive } from 'vue';

const message = ref('this is vue3')
const space = ref(0)

function spacePressed(){
    space.value++
    message.value = "Space pressed "+ space.value +" times."
}

function pressedWhat(event){
 
    message.value = "you pressed "+ event.key +" ."
}

function ctrlRightClick(){
 
    message.value = "Ctrl + Right click."
}
 

function divClick(){
    alert('Div Click');
}

function buttonClick(){
    alert('Button Click');
}
 
</script>


<template>



<hr>
<h4 class="text-center"> Event Modifier </h4>
<hr>
 
 

<div class="row">
    <div class="col-md-4"></div>
    <div class="col-md-3 text-center">
        <p> {{ message }}</p>

        <input type="text" @keyup.space="spacePressed()" class="form-control">
        <input type="text" @keyup="pressedWhat($event)" class="form-control mt-4">
        <button @click.ctrl.right="ctrlRightClick()" class="btn btn-primary mt-4"> Ctrl + Right </button>


        <div @click="divClick()" class="col-md-12 bg-light p-4 mt-4 border border-primary">
            <button @click.stop="buttonClick()" class="btn btn-primary m-4"> Button </button>
        </div>
    </div>
   
    </div>

 
    </template>