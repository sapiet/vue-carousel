<template src="./App.html" />
<style lang="scss" src="./App.scss"/>

<script>
import Carousel from './components/carousel/Carousel.vue'
import CarouselSlide from './components/carousel/Carouselslide.vue'

export default {
    components: {
        Carousel,
        CarouselSlide
    },
    data() {
        return {
            slides: [
                {image: 'https://picsum.photos/600/200?random=1', caption: 'Lorem ipsum dolor sit amet, consectetur adipisicing elit. Dolorem, mollitia?'},
                {image: 'https://picsum.photos/600/200?random=2', caption: 'Ipsum dolor sit amet, consectetur adipisicing elit. Dolorem, mollitia?'},
                {image: 'https://picsum.photos/600/200?random=3', caption: 'Lorem ipsum dolor sit amet, consectetur adipisicing elit. Dolorem, mollitia?'},
                {image: 'https://picsum.photos/600/200?random=4', caption: 'Ipsum dolor sit amet, consectetur adipisicing elit. Dolorem, mollitia?'},
                {image: 'https://picsum.photos/600/200?random=5', caption: 'Lorem ipsum dolor sit amet, consectetur adipisicing elit. Dolorem, mollitia?'},
                {image: 'https://picsum.photos/600/200?random=6', caption: 'Ipsum dolor sit amet, consectetur adipisicing elit. Dolorem, mollitia?'},
            ]
        }
    }
}
</script>
