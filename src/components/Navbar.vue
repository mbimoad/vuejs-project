<template>  
    <!-- Page navigation -->
    <nav class="navbar navbar-expand-lg navbar-light fixed-top" data-spy="affix" data-offset-top="0">
        <div class="container">
            <a class="navbar-brand" href="#"><img src="../assets/imgs/logo.svg" alt=""></a>
            <button class="navbar-toggler" type="button" data-toggle="collapse" data-target="#navbarSupportedContent" aria-controls="navbarSupportedContent" aria-expanded="false" aria-label="Toggle navigation">
                <span class="navbar-toggler-icon"></span>
            </button>

            <div class="collapse navbar-collapse" id="navbarSupportedContent">
                <ul class="navbar-nav ml-auto align-items-center">
                    <span v-for="i in menu">
                        <li class="nav-item">
                            <a class="nav-link" :href="lowercase(i)">{{ i }}</a>
                        </li>
                    </span>
                    <li class="nav-item">
                        <a class="- btn btn-primary rounded ml-4" href="mailto:bimoadjie19@gmail.com">Contact Me</a>
                    </li>
                </ul>
            </div>
        </div>          
    </nav>
    <!-- End of page navibation -->
</template>

<script>
export default {
    data() {
        return {
            menu: ['Home','About','Service','Portfolio','Experience']
        }
    },
    methods: {
        lowercase(string) {
            return `#` + string.toLowerCase(); 
        }
    },
    mounted() {
        
        $(document).ready(function(){
        $(".nav-link").on('click', function(event) {

                if (this.hash !== "") {

                    event.preventDefault();

                    var hash = this.hash;

                    $('html, body').animate({
                        scrollTop: $(hash).offset().top
                    }, 700, function(){
                        window.location.hash = hash;
                    });
                } 
            });
        });
    },
}
</script>

<style>

</style>