<script setup>
const bgInfo = 'background-color: rgb(112, 112, 201)';
const bgWarning = 'background-color: rgb(255, 169, 8)';
const bgSuccess = 'background-color: rgb(71, 170, 71)';

const weekday = false;

const message = 'success';

const  colors = {
    borderTop:'5px solid red',
    backgroundColor:'rgb(255, 169, 8)',
    color:'red',
    fontSize:'20px'

}

if('success'==message){

    colors.borderTop = '5px solid greenyellow';
    colors.backgroundColor = 'green';
    colors.color = 'greenyellow';
    colors.fontSize = '30px'
}
</script>

<template>

<hr>
<h4 class="text-center"> Style Binding </h4>
<hr>


 <!-- =========================================  -->
 <!-- =========================================  -->
 <div class="row">

  <div class="col-md-4">
    <div class="col-md-12 h-100" :style="bgInfo"> 
        <p>
          Lorem ipsum dolor sit amet consectetur adipisicing elit. Modi voluptatem odit, nisi explicabo suscipit culpa quo sunt cupiditate tenetur impedit accusamus magni. Perferendis minus quam praesentium itaque vitae hic dolores.
        </p>
    </div>
  </div>

  <div class="col-md-4">
    <div class="col-md-12 h-100" :style="bgWarning"> 
      <p>
          Lorem ipsum dolor sit amet consectetur adipisicing elit. Modi voluptatem odit, nisi explicabo suscipit culpa quo sunt cupiditate tenetur impedit accusamus magni. Perferendis minus quam praesentium itaque vitae hic dolores.
        </p> </div>
  </div>

  <div class="col-md-4">
    <div class="col-md-12 h-100" :style="bgSuccess"> 
      <p>
          Lorem ipsum dolor sit amet consectetur adipisicing elit. Modi voluptatem odit, nisi explicabo suscipit culpa quo sunt cupiditate tenetur impedit accusamus magni. Perferendis minus quam praesentium itaque vitae hic dolores.
        </p> </div>
  </div>


 </div>

  <!-- =========================================  -->
 <!-- ==============  //  ======================  -->




 <div class="row mt-4">
  <!-- <div class="col-md-12" :style="weekday==true?[bgWarning,'font-size:20px']:[bgSuccess,'font-size:40px']"> -->
  <div class="col-md-12" :style="[weekday==true?bgWarning:bgSuccess,weekday==true?'font-size:20px':'font-size:40px;']">
      <p class="text-center">
        It's a weekend.
      </p>
  </div>
 </div>





 
 <div class="row mt-4">
  <div class="col-md-6  rounded " :style="colors">
      <h2 class="text-center">
        This is alert message.
      </h2>
  </div>
 </div>

</template>

<style scoped>

</style>
