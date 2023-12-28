<template>
    <div class="catalog__menu">
        <div class="catalog__item" v-for="item in items" :key="item.id">
            <img class="catalog__img" :src="require(`@/images/${item.path}`)"/>
            <div class="catalog__img-info-up">
                <p class="catalog__weight">{{item.weigh}}</p>
                <p class="catalog__kcal">{{item.kcal}}</p>
            </div>
            <span class="catalog__span"></span>
            <div class="catalog__img-info-bottom">
                <h1 class="catalog__name">{{item.name}}</h1>
                <h2 class="catalog__price">{{item.price}}</h2>
            </div>
            <p class="catalog__text">{{item.text}}</p>
        </div>
    </div>
</template>

<script>
    export default {
        props: ['items'],
        data() {
            return {
                
            }
        }
    }
</script>

<style>
        .catalog__menu {
            display: grid;
            grid-template-columns: repeat(auto-fill, minmax(200px, 1fr)); 
            grid-template-rows: repeat(auto-fill, minmax(303px, 2fr));
            grid-gap: 10px;
            width: 835px;
            height: 1600px;
            margin-top: 28px;
        }

        .catalog__item {
            border-radius: 14px;
            background-color: #F3F4F5;
            height: 303px;
        }

        .catalog__img {
            width: 200px;
            height: 175px;
            object-fit: cover;
        }

        .catalog__img-info-up {
            display: flex;
            flex-direction: row;
            justify-content: space-between;
            margin: 15px 16px;
        }

        .catalog__weight {
            color: #A8B4C5;
            font-size: "Inter", sans-serif;
            font-size: 12px;
            line-height: 15px;
            margin: 0;
        }

        .catalog__kcal {
            color: #A8B4C5;
            font-size: "Inter", sans-serif;
            font-size: 12px;
            line-height: 15px;
            margin: 0;
        }

        .catalog__span {
            display: block;
            border: solid 1px #C6D1E0;
            width: 168px;
            margin: 0 auto;
        }

        .catalog__name {
            font-family: 'Inter', sans-serif;
            font-size: 14px;
            font-weight: 500;
            line-height: 18px;
            margin: 0;
            color: #191919;
;
        }

        .catalog__price {
            font-family: 'Inter', sans-serif;
            font-size: 14px;
            font-weight: 600;
            line-height: 18px;
            margin: 0;
            color: #191919;
        }

        .catalog__img-info-bottom {
            display: flex;
            justify-content: space-between;
            margin: 15px 16px;
            width: 168px;
        }

        .catalog__text {
            color: #A8B4C5;
            font-family: 'Inter', sans-serif;
            font-size: 12px;
            font-weight: 400;
            line-height: 15px;
            margin: 0 16px;
            padding-bottom: 16px;
        }
</style>