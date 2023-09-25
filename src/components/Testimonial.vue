<template>
  
    <!-- Testmonial Section -->
    <section id="experience" class="section">
        <div class="container text-center">
            <h6 class="section-title mb-4">Working Experience</h6>
            <p class="mb-5 pb-4">Here are some of the experiences i managed to achieve</p>

            <div id="carouselExampleIndicators" class="carousel slide" data-ride="carousel">
                <!-- Carousel DOt -->
                
                <ol class="carousel-indicators">
                    <li v-for="isi,index in data" :key="index" data-target="#carouselExampleIndicators" :class="{active: index==0}" :data-slide-to="index"></li>
                </ol>

                <div class="carousel-inner">
                    <!-- Carousel Item -->
                    <div class="carousel-item" v-for="isi,index in data" :key="isi.title" :class="{active: index==0}">
                        <div class="card testmonial-card border">
                            <div class="card-body">
                                <img :src="Gambar(isi.image)" alt="">
                                <h1 class="title">{{ isi.title }}</h1>
                                <h1 class="subtitle">{{ isi.date }}</h1>
                                <h1 class="subtitle">{{ isi.position }}</h1>
                                <p>{{ isi.description }}</p>
                            </div>
                        </div>
                    </div>
                    <!-- End of carousel item -->
                </div>

            </div>
        </div>
    </section>
    <!-- End of testmonial section -->

</template>

<script>
import {ref} from 'vue';
import JSON from '../json/expe.json'
export default {
    setup() {
        const data = ref(JSON); 
        const panjang = data.value.length; 
        
        const Gambar = (path) => {
            let file = ''; 
            try {
                file = require(`@/assets/${path}`);
            } catch(e) {
                file = ''; 
            }
            return file;
        }
        return {
            data, 
            Gambar,
            panjang
        }
    }
}
</script>

<style>

</style>