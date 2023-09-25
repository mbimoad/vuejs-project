<template>
    <!-- Page Header -->
    <header class="header" id="home">
        <div class="container">
            <div class="infos">
                <h6 class="subtitle">hello,I'm</h6>
                <h6 class="title">{{name}}</h6>
                <p>Full Stack Web Developer</p>

                <div class="buttons pt-3">
                    <a href="mailto:bimoadjie19@gmail.com" class="btn btn-primary rounded">HIRE ME</a>
                    <a href="https://drive.google.com/uc?id=1LL4zcQx5eZqjbE9i-MaUs9_Q2RbR2KYp&export=download" class="btn btn-dark rounded">DOWNLOAD CV</a>
                </div>      

                <div class="socials mt-4">
                    <a class="social-item" href="mailto:bimoadjie19@gmail.com"><i class="ti-google"></i></a>
                    <a class="social-item" href="https://github.com/mbimoad"><i class="ti-github"></i></a>
                    <a class="social-item" href="https://instagram.com/mbimoad"><i class="ti-instagram"></i></a>
                </div>
            </div>              
            <div class="img-holder">
                <img src="../assets/imgs/man.svg" alt="">
            </div>      
        </div>  

        <!-- Header-widget -->
        <div class="widget">
            <div class="widget-item">
                <h2>20++</h2>
                <p>Happy Clients</p>
            </div>
            <div class="widget-item">
                <h2>30++</h2>
                <p>Project Completed</p>
            </div>
        </div>
    </header>
    <!-- End of Page Header -->
</template>

<script>
export default {
    props: ['name'],
}
</script>

<style>

</style>