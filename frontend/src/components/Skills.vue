<template>
  
    <!-- Skills section -->
    <section class="section">
        <div class="container text-center">
            <h6 class="subtitle">Skills</h6>
            <h6 class="section-title mb-4">Why Choose me</h6>
            <p class="mb-5 pb-4">Here are some of the capabilities and technologies I've used</p>

            <div class="row text-left">
                <div class="col-sm-6" v-for="i in data" :key="i.title">
                    <h6 class="mb-3">{{i.title}}</h6>
                    <div class="progress">
                        <div class="progress-bar bg-primary" role="progressbar" :style="chart(i.chart)" aria-valuenow="25" aria-valuemin="0" aria-valuemax="100"><span>89%</span></div>
                    </div>
                </div>
            </div>  
        </div>
    </section>
    <!-- End of Skills sections -->
</template>

<script>
import {ref,onMounted} from 'vue'; 
import JSON from '../json/skill.json';
export default {
    
    setup() {
        const data  = ref(JSON); 
        const chart = (value) => `width: ${value}%`; 
        return {
            chart, 
            data
        }

    }
}
</script>

<style>

</style>