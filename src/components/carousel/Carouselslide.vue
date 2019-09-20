<template src="./Carouselslide.html"/>
<style lang="scss" src="./Carouselslide.scss"/>

<script>
export default {
    props: {
        index: {
            type: Number,
            default: 0
        }
    },
    computed: {
        visible() {
            return this.index === this.$parent.index
        },

        transition() {
            return this.$parent.direction ? 'slide-' + this.$parent.direction : null
        }
    }
}
</script>
