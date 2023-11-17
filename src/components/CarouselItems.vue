<template>
    <div class="carousel">
        <button class="carousel__btn" @click="prevSlide"><img :src="arrowLeft"/></button>
        <img :src="slides[currentIndex]" class="carousel__img"/>
        <button class="carousel__btn" @click="nextSlide"><img :src="arrowRight"/></button>
    </div>
</template>

<script>
    import img1 from '../images/img-1.png';
    import img2 from '../images/img-2.png';

    import arrowLeft from '@/images/arrow-left.svg';
    import arrowRight from '@/images/arrow-right.svg';

    export default {
        data() {
            return {
                slides: [
                    img1,
                    img2,
                ],
                currentIndex: 0,
                arrowLeft: arrowLeft,
                arrowRight: arrowRight,
            }
        },
        methods: {
            prevSlide() {
                this.currentIndex = (this.currentIndex - 1 + this.slides.length) % this.slides.length;
            },
            nextSlide() {
                this.currentIndex = (this.currentIndex + 1) % this.slides.length;
            },
        }
        }
</script>

<style>
    .carousel {
        margin: 27px auto;
        width: 1200px;
        display: flex;
        gap: 20px;
        align-items: center;
    }

    .carousel__img {
        height: 238px;
        width: 1080px;
        border-radius: 15px;
    }

    .carousel__btn {
        background-color: transparent;
        border: none;
    }
</style>