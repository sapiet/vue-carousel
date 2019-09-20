<template src="./Carousel.html"/>
<style lang="scss" src="./Carousel.scss"/>

<script>
export default {
    data() {
        return {
            index: 0,
            slides: [],
            direction: null
        }
    },
    computed: {
        count() {
            return this.slides.length;
        },

        maxIndex() {
            return this.count - 1;
        }
    },
    watch: {
        slides() {
            if (this.index >= this.slidesCount) {
                this.index = this.slidesCount - 1;
            }
        }
    },
    mounted() {
        this.slides = this.$children;
    },
    methods: {
        previous() {
            this.direction = 'left';
            this.index = this.index === 0 ? this.maxIndex : this.index - 1;
        },

        next() {
            this.direction = 'right';
            this.index = this.index >= this.maxIndex ? 0 : this.index + 1;
        },

        goTo(n) {
            this.direction = n > this.index ? 'right' : 'left';
            this.index = n;
        },

        isSlideActive(n) {
            return n === this.index;
        }
    }
}
</script>
