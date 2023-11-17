<template>
    <HeaderItems />
    <CarouselItems />
    <FooterItems />
</template>

<script>
    import HeaderItems from './components/HeaderItems.vue';
    import FooterItems from './components/FooterItems.vue';
    import CarouselItems from './components/CarouselItems.vue';

    export default {
        components: {
            HeaderItems,
            FooterItems,
            CarouselItems,
}
    }
</script>

<style>
  @import url('https://fonts.googleapis.com/css2?family=Inter&display=swap');

</style>
