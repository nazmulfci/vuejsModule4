<script setup>
import { ref,reactive } from 'vue';
const accordionIndex = reactive([
    false,false,false,false
]);

function toggle(index){
    accordionIndex[index] = !accordionIndex[index]
}
</script>


<template>

<hr>
<h4 class="text-center"> Creating an accordion with Toggle </h4>
<hr>
 
 

<div class="row">
    <div class="col-md-12">



            <div id="accordion">
                    <div class="card">
                        <div class="card-header" @click="toggle(0)">
                        <h5 class="mb-0">
                            Collapsible Group Item #1
                        </h5>
                        </div>

                        <div>
                        <div class="card-body" v-show="accordionIndex[0]">
                            Anim pariatur cliche reprehenderit, enim eiusmod high life accusamus terry richardson ad squid. 3 wolf moon officia aute, non cupidatat skateboard dolor brunch. Food truck quinoa nesciunt laborum eiusmod. Brunch 3 wolf moon tempor, sunt aliqua put a bird on it squid single-origin coffee nulla assumenda shoreditch et. Nihil anim keffiyeh helvetica, craft beer labore wes anderson cred nesciunt sapiente ea proident. Ad vegan excepteur butcher vice lomo. Leggings occaecat craft beer farm-to-table, raw denim aesthetic synth nesciunt you probably haven't heard of them accusamus labore sustainable VHS.
                        </div>
                        </div>
                    </div>
                    <div class="card">
                        <div class="card-header"  @click="toggle(1)">
                        <h5 class="mb-0">
                            Collapsible Group Item #2
                        </h5>
                        </div>
                        <div>
                        <div class="card-body"  v-show="accordionIndex[1]">
                            Anim pariatur cliche reprehenderit, enim eiusmod high life accusamus terry richardson ad squid. 3 wolf moon officia aute, non cupidatat skateboard dolor brunch. Food truck quinoa nesciunt laborum eiusmod. Brunch 3 wolf moon tempor, sunt aliqua put a bird on it squid single-origin coffee nulla assumenda shoreditch et. Nihil anim keffiyeh helvetica, craft beer labore wes anderson cred nesciunt sapiente ea proident. Ad vegan excepteur butcher vice lomo. Leggings occaecat craft beer farm-to-table, raw denim aesthetic synth nesciunt you probably haven't heard of them accusamus labore sustainable VHS.
                        </div>
                        </div>
                    </div>
                    <div class="card">
                        <div class="card-header"  @click="toggle(2)">
                        <h5 class="mb-0">
                            Collapsible Group Item #3
                        </h5>
                        </div>
                        <div>
                        <div class="card-body"  v-show="accordionIndex[2]">
                            Anim pariatur cliche reprehenderit, enim eiusmod high life accusamus terry richardson ad squid. 3 wolf moon officia aute, non cupidatat skateboard dolor brunch. Food truck quinoa nesciunt laborum eiusmod. Brunch 3 wolf moon tempor, sunt aliqua put a bird on it squid single-origin coffee nulla assumenda shoreditch et. Nihil anim keffiyeh helvetica, craft beer labore wes anderson cred nesciunt sapiente ea proident. Ad vegan excepteur butcher vice lomo. Leggings occaecat craft beer farm-to-table, raw denim aesthetic synth nesciunt you probably haven't heard of them accusamus labore sustainable VHS.
                        </div>
                        </div>
                    </div>
            </div>




    </div>
</div>
    </template>