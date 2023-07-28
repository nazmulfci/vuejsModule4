<script setup>

const items = [1,2,3,4,5];
const languages = [
    'Html',
    'Html5',
    'css',
    'css3',
    'javascript',
    'jquery',
];
const tasks = [
    {id:1,title:'Meeting with client',status:"Pending"},
    {id:2,title:'Business analysis & wareframing',status:"Completed"},
    {id:3,title:'UI/UX design',status:"Pending"},
    {id:4,title:'Business logic analysis',status:"In Progress"},
];

function getCompletedTask(){
    return tasks.filter(task => 'Completed'==task.status);
}

function getPendingTask(){
    return tasks.filter(task => 'Pending'==task.status);
}
</script>

<template>

<hr>
<h4 class="text-center"> Simple loop or list rendering </h4>
<hr>

<!-- if you miss to use key attribute about multiple loop -->
<h2> Completed Task </h2>
<div v-for="task,index in getCompletedTask()" :key="task.id">
    <button class="btn btn-primary mb-4">{{ task.id }}. {{ task.title }} </button>
</div>
<h2> Pending Task </h2>
<div v-for="task,index in getPendingTask()" :key="task.id">
    <button class="btn btn-primary mb-4">{{ task.id }}. {{ task.title }} </button>
</div>



<!-- if you miss to use key attribute about multiple loop -->
<!-- <div v-for="language,index in languages" :key="language">
    <button class="btn btn-primary mb-4">{{ index+1 }}. {{ language }} </button>
</div> -->



<!-- 
<p v-for="n in 10" :key="n"> 
    <button class="btn btn-primary mb-4">  {{ n }}  </button>
</p> -->

<!-- 

<p v-for="item in items"  :key="item"> 
      Item - {{ item }}  
</p> -->





</template>

<style scoped>

</style>
