<template>
    <section class="menu">
        <h1 class="menu__title">Меню</h1>
        <div class="menu__items">
            <p class="menu__item">Lorem Ipsum</p>
            <p class="menu__item">Lorem Ipsum</p>
            <p class="menu__item">Lorem Ipsum</p>
            <p class="menu__item">Lorem Ipsum</p>
            <p class="menu__item">Lorem Ipsum</p>
            <p class="menu__item">Lorem Ipsum</p>
            <p class="menu__item">Lorem Ipsum</p>
            <p class="menu__item">Lorem Ipsum</p>
            <p class="menu__item">Lorem Ipsum</p>
            <p class="menu__item">Lorem Ipsum</p>
            <p class="menu__item">Lorem Ipsum</p>
            <p class="menu__item">Lorem Ipsum</p>
            <p class="menu__item">Lorem Ipsum</p>
            <p class="menu__item">Lorem Ipsum</p>
            <p class="menu__item">Lorem Ipsum</p>
            <p class="menu__item">Lorem Ipsum</p>
        </div>
    </section>
</template>

<script>
    export default {

    }
</script>

<style>
    .menu {
        display: flex;
        flex-direction: column;
        background-color: #fff;
        border-radius: 16px;
        min-width: 285px;
        max-width: 285px;
        height: 1710px;
        gap: 36px;
    }

    .menu__title {
        color: #191919;
        margin: 30px 0 0 30px;
    }

    .menu__items {
        background-color: #F3F4F5;
        width: 225px;
        height: 1600px;
        display: flex;
        flex-direction: column;
        color: #728299;
        font-size: 14px;
        font-weight: 500;
        line-height: 18px;
        letter-spacing: 0;
        text-align: left;
        gap: 18px;
        border-radius: 14px;
        margin: 0 auto;
        padding-top: 10px;
    }

    .menu__item {
        margin: 0;
        padding-left: 23px;
    }
</style>