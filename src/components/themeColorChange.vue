<script setup>
import {ref,reactive} from 'vue'
const theme = ref('success')

const themeColors = reactive(
    {
    bgColor:'bg-success',
    btnColor:'btn-success',
    alertColor:'alert-success',    
    borderColor:'border-success',    
    textColor:'text-success',    
    });

           
    function setThemeColor(e){
    theme.value = e;
    console.log(theme.value)
}

    if(theme.value=='info'){
        themeColors.bgColor='bg-info'
        themeColors.btnColor = 'btn-info'
        themeColors.alertColor = 'alert-info'    
        themeColors.borderColor = 'border-info'    
        themeColors.textColor = 'text-info'    
        }

    if('warning'==theme.value){
        themeColors.bgColor='bg-warning'
        themeColors.btnColor = 'btn-warning'
        themeColors.alertColor = 'alert-warning'    
        themeColors.borderColor = 'border-warning'    
        themeColors.textColor = 'text-warning'    
        }

    if('danger'==theme.value){
        themeColors.bgColor='bg-danger'
        themeColors.btnColor = 'btn-danger'
        themeColors.alertColor = 'alert-danger'    
        themeColors.borderColor = 'border-danger'    
        themeColors.textColor = 'text-danger'    
        }

 
</script>

<template>
<hr>
<h4 class="text-center"> Theme color change </h4>
<hr>
 <div class="row">
    <div class="col-md-6"></div>
    <div class="col-md-3"></div>
    <div class="col-md-3">
        <div @click="setThemeColor('success')" class="box bg-success"></div>
        <div @click="setThemeColor('info')" class="box bg-info"></div>
        <div @click="setThemeColor('warning')" class="box bg-warning"></div>
        <div @click="setThemeColor('danger')" class="box bg-danger"></div>
    </div>
 </div>




 <div class="row mt-4">
    <div class="col-md-12 header text-light" :class="themeColors.bgColor">
        <h1> Doofaz IT </h1>
    </div>
 </div>
 <div class="row">
    <div class="col-md-12 hero pt-4 pb-4" :class="themeColors.alertColor">
        <h2 class="mt-4"> Doofaz IT </h2>
        <p class="mb-4">Lorem ipsum dolor sit amet consectetur adipisicing elit. Eveniet, ipsum neque quasi praesentium consectetur sint. Ut ipsum omnis assumenda quas similique consequuntur dolor nisi enim maiores doloremque animi, ipsam incidunt.</p>
        <button class="btn"  :class="themeColors.btnColor"> Show More </button>
    </div>
 </div>

 <div class="container mt-5">
    <div class="row">
       
        <div class="col-md-3" v-for="n in 4">
        <div class="col-md-12 border"  :class="themeColors.borderColor">
            <div class="col-12 circle rounded rounded-circle" :class="themeColors.bgColor"></div>
            <h4  :class="themeColors.textColor"> This is heading. </h4>
            <p  :class="themeColors.textColor"> Lorem ipsum dolor sit amet consectetur, adipisicing elit. Exercitationem est tenetur maxime delectus, nemo iste iusto incidunt deserunt ea assumenda labore dicta consectetur error non quidem soluta quos voluptates ab. </p>
        </div>
        </div>
       
        

    </div>
 </div>



 <div class="row mt-5">
    <div class="col-md-12 text-center text-light" :class="themeColors.bgColor">
        <p> This is footer </p>
    </div>
 </div>
</template>

<style>
.circle{
    height:200px;
}
.header{
    height:50px;
}
.hero{
    height: 300px;
}
.box{
    width:30px;
    height:30px;
    /* border: 1px solid #615f5f; */
    float: left;
    margin-right: 10px;
    cursor: pointer;
}
</style>