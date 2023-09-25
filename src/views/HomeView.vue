<template>
    <Navbar />
    <Header name="mbimoad" />
    <About />
    <Services />
    <Skills />
    <Portfolio />
    <Testimonial />
    <Footer />
</template>

<script>
import About from '../components/About.vue';
import Navbar from '../components/Navbar.vue';
import Header from '../components/Header.vue';
import Services from '../components/Services.vue';
import Skills from '../components/Skills.vue';
import Portfolio from '../components/Portfolio.vue';
import Testimonial from '../components/Testimonial.vue';
import Blog from '../components/Blog.vue';
import Hireme from '../components/Hireme.vue';
import Contact from '../components/Contact.vue';
import Footer from '../components/Footer.vue';
export default {
    components: {
        Navbar,
        Header,
        About,
        Services,
        Skills,
        Portfolio,
        Testimonial,
        Blog,
        Hireme,
        Contact,
        Footer
    }
}
</script>

<style>

</style>