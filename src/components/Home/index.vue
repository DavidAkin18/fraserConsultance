<template>
    <div>
        <Header/>
        <Hero/>
        <Services/>
        <Sectors/>
        <Testimonial />
        <About />
        <News />
        <Footer />
    </div>
</template>

<script>
import Header from './Header.vue';
import About from './About.vue';
import Hero from './Hero.vue';
import News from './News.vue';
import Sectors from './Sectors.vue';
import Services from './Services.vue';
import Testimonial from './Testimonial.vue';
import Footer from './Footer.vue';
export default {
   components:{
        Header,
        About,
        Hero,
        News,
        Sectors,
        Services,
        Testimonial,
        Footer
   }
}
</script>

<style>

</style>