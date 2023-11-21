<template>
    <div class="carousel">
        <button class="carousel__btn" @click="prevSlide"><img :src="arrowLeft"/></button>
        <div class="carousel__images">
            <img :src="slides[prevIndex]" class="carousel__img carousel__img_previous"/>
            <img :src="slides[currentIndex]" class="carousel__img"/>
            <img :src="slides[nextIndex]" class="carousel__img carousel__img_next"/>
        </div>
        <button class="carousel__btn" @click="nextSlide">
        <img :src="arrowRight"/></button>
    </div>
    <div class="carousel__circles">
        <img v-for="(slide, index) in slides" :key="index" :src="index === currentIndex ? circleOn : circleEmpty" />
    </div>
</template>

<script>
    import img1 from '../images/img-1.png';
    import img2 from '../images/img-2.png';
    import img3 from '../images/img-3.png';

    import circleOn from '../images/circle-on.svg';
    import circleEmpty from '../images/circle-empty.svg';

    import arrowLeft from '@/images/arrow-left.svg';
    import arrowRight from '@/images/arrow-right.svg';

    export default {
        data() {
            return {
                slides: [
                    img1,
                    img2,
                    img3,
                ],
                currentIndex: 0,
                arrowLeft: arrowLeft,
                arrowRight: arrowRight,
                circleEmpty: circleEmpty,
                circleOn: circleOn,
                images: [
                    circleEmpty,
                    circleEmpty,
                    circleOn,
                ]
            }
        },
        methods: {
            prevSlide() {
                if (this.currentIndex == 0) {
                    this.currentIndex = this.slides.length - 1;
                } else {
                    this.currentIndex--;
                }
            },
            nextSlide() {
                if (this.currentIndex == this.maxIndex) {
                    this.currentIndex = 0;
                } else {
                    this.currentIndex++;
                }
            },
        },
        computed: {
            maxIndex() {
                return this.slides.length - 1;
            },

            nextIndex() {
                if (this.currentIndex === this.slides.length - 1) {
                    return 0
                } else {
                    return this.currentIndex + 1
                }
            },

            prevIndex() {
                if (this.currentIndex === 0) {
                    return this.slides.length - 1
                } else {
                    return this.currentIndex - 1
                }
            }
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

    .carousel__images {
        position: relative;
    }

    .carousel__img {
        height: 238px;
        width: 1080px;
        border-radius: 15px;
    }

    .carousel__img_previous {
        position: absolute;
        top: 0;
        left: calc(-100% - 20px);
        z-index: -1;
    }

    .carousel__img_next {
        position: absolute;
        top: 0;
        right: calc(-100% - 20px);
        z-index: -1;
    }

    .carousel__btn {
        background-color: transparent;
        border: none;
    }

    .carousel__circles {
        display: flex;
        justify-content: center;
        gap: 5px;
    }
</style>