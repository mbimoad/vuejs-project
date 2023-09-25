<template>
   <!-- Portfolio section -->
    <section id="portfolio" class="section">
        <div class="container text-center">
            <h6 class="subtitle">Portfolio</h6>
            <h6 class="section-title mb-4">Check My Wonderful Works</h6>
            <p class="mb-5 pb-4">The following is a portfolio of applications that I have worked on.</p>

            <div class="row">
                
                <div class="col-sm-4" v-for="i in data" :key="i.title">
                    <div class="img-wrapper">
                        <img :src="Gambar(i.image)" alt="">
                        <div class="overlay">
                            <div class="overlay-infos">
                                <h5>{{ i.title }}</h5>
                                <a :href="i.link"><i class="ti-link"></i></a>
                            </div>  
                        </div>
                    </div>      
                </div>



            </div>
        </div>
    </section>
    <!-- End of portfolio section -->

</template>

<script>
import {ref} from 'vue';
import JSON from '../json/port.json'
export default {
    setup() {
        const data = ref(JSON); 
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
            Gambar
        }
    }
}
</script>

<style>

</style>