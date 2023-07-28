<script setup>
import { ref,reactive } from 'vue';


const accordions = reactive([
    {
        id:1,
        headding:'What is Term?',
        description:'Lorem ipsum dolor sit amet, consectetur adipisicing elit. Assumenda excepturi vel sed accusamus harum incidunt ex, repellat tenetur cumque velit repudiandae error dignissimos fugit quaerat maxime sequi natus necessitatibus sit.',
        isOpen:false
    },
    {
        id:2,
        headding:'When to use accordion components?',
        description:'Lorem ipsum dolor sit amet, consectetur adipisicing elit. Assumenda excepturi vel sed accusamus harum incidunt ex, repellat tenetur cumque velit repudiandae error dignissimos fugit quaerat maxime sequi natus necessitatibus sit.',
        isOpen:false
    },
    {
        id:3,
        headding:'How can it be define?',
        description:'Lorem ipsum dolor sit amet, consectetur adipisicing elit. Assumenda excepturi vel sed accusamus harum incidunt ex, repellat tenetur cumque velit repudiandae error dignissimos fugit quaerat maxime sequi natus necessitatibus sit.',
        isOpen:false
    },
    {
        id:4,
        headding:'What is the banifits of accordions?',
        description:'Lorem ipsum dolor sit amet, consectetur adipisicing elit. Assumenda excepturi vel sed accusamus harum incidunt ex, repellat tenetur cumque velit repudiandae error dignissimos fugit quaerat maxime sequi natus necessitatibus sit.',
        isOpen:false
    },
])

const activeIndex = ref(0);
</script>


<template>



<hr>
<h4 class="text-center"> Creating an accordion with (Loop, Event, Reactivity) </h4>
<hr>
 
 

<div class="row">
    <div class="col-md-6">
    <div class="col-md-12">



            <div id="accordion">
                    <div class="card" v-for="accordion in accordions" :key="accordion.id">
                        <div class="card-header" @click="accordion.isOpen = !accordion.isOpen">
                        <h5 class="mb-0">
                            {{ accordion.headding }}
                        </h5>
                        </div>

                        <div>
                        <div class="card-body" v-show="accordion.isOpen">
                            {{ accordion.description }}
                        </div>
                        </div>
                    </div>
                    
                    
            </div>
            </div>




    </div>


    <div class="col-md-6 ">
    <div class="col-md-12">



        <div id="accordion">
                    <div class="card" v-for="(accordion,index) in accordions" :key="accordion.id">
                        <div class="card-header" @click="activeIndex=index">
                        <h5 class="mb-0">
                            {{ accordion.headding }}
                        </h5>
                        </div>

                        <div>
                        <div class="card-body" v-show="activeIndex==index">
                            {{ accordion.description }}
                        </div>
                        </div>
                    </div>
                    
                    
            </div>
            </div>




    </div>
</div>
    </template>