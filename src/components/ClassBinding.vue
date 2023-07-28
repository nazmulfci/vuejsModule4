<script setup>
const primaryColor = 'bg-primary';
const warningColor = 'bg-warning';
const infoColor = 'bg-info';
const successColor = 'bg-success';

const textWhite = 'text-white';


const weekday = false;

const colors = {
  bgColor:'alert-danger',
  borderColor:'border-danger',
  textColor:'text-danger'
};
const messageType = 'error';

if('success'==messageType){
  colors.bgColor = 'alert-success';
  colors.borderColor = 'border-success';
  colors.textColor = 'text-success';
}

if('warning'==messageType){
  colors.bgColor = 'alert-warning';
  colors.borderColor = 'border-warning';
  colors.textColor = 'text-warning';
}
</script>

<template>

<hr>
<h4 class="text-center"> Class Binding </h4>
<hr>


 <!-- =========================================  -->
 <!-- =========================================  -->
 <div class="row">

  <div class="col-md-4">
    <div class="col-md-12 h-100" :class="primaryColor,textWhite"> 
        <p>
          Lorem ipsum dolor sit amet consectetur adipisicing elit. Modi voluptatem odit, nisi explicabo suscipit culpa quo sunt cupiditate tenetur impedit accusamus magni. Perferendis minus quam praesentium itaque vitae hic dolores.
        </p>
    </div>
  </div>

  <div class="col-md-4">
    <div class="col-md-12 h-100" :class="warningColor"> 
      <p>
          Lorem ipsum dolor sit amet consectetur adipisicing elit. Modi voluptatem odit, nisi explicabo suscipit culpa quo sunt cupiditate tenetur impedit accusamus magni. Perferendis minus quam praesentium itaque vitae hic dolores.
        </p> </div>
  </div>

  <div class="col-md-4">
    <div class="col-md-12 h-100" :class="successColor,textWhite"> 
      <p>
          Lorem ipsum dolor sit amet consectetur adipisicing elit. Modi voluptatem odit, nisi explicabo suscipit culpa quo sunt cupiditate tenetur impedit accusamus magni. Perferendis minus quam praesentium itaque vitae hic dolores.
        </p> </div>
  </div>


 </div>

  <!-- =========================================  -->
 <!-- ==============  //  ======================  -->




  <!-- =========================================  -->
 <!-- =========================================  -->


 <div class="row mt-4">
  <div class="col-md-12" :class="[weekday?'bg-danger':'bg-success',weekday?'text-warning':'text-light']">
      <p class="text-center">
        It's a weekend.
      </p>
  </div>
 </div>

  <!-- =========================================  -->
 <!-- ===============  //  =====================  -->


  <!-- =========================================  -->
 <!-- =========================================  -->


 <div class="row mt-4">
  <div class="col-md-6 border-top rounded " :class="colors.bgColor,colors.borderColor,colors.textColor">
      <h2 class="text-center">
        This is alert message.
      </h2>
  </div>
 </div>

  <!-- =========================================  -->
 <!-- ===============  //  =====================  -->

</template>

<style scoped>
 .h-100{
  height: 100px;
 }
</style>
