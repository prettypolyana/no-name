<template>
    <section class="menu">
        <h1 class="menu__title">Меню</h1>
        <div class="menu__items">
            <p class="menu__item">Кофе и чай</p>
            <p class="menu__item">Холодные напитки</p>
            <p class="menu__item">Комбо</p>
            <p class="menu__item">Shoko Go</p>
            <p class="menu__item">Конструктор завтраков</p>
            <p class="menu__item">Завтраки весь день</p>
            <p class="menu__item">Блинчики</p>
            <p class="menu__item">Пицца от Eazzy Pizza & Gelato</p>
            <p class="menu__item">Супы</p>
            <p class="menu__item">Горячие блюда</p>
            <p class="menu__item">Сэндвичи</p>
            <p class="menu__item">Только в доставке</p>
            <p class="menu__item">Салаты</p>
            <p class="menu__item">Десерты</p>
            <p class="menu__item">Добавки и соусы</p>
            <p class="menu__item">Указаны розничные цены</p>
        </div>
    </section>
</template>

<script>
    export default {

    }
</script>

<style>
    @import url('https://fonts.googleapis.com/css2?family=Playfair+Display:wght@800&display=swap');

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
        font-family: 'Playfair Display', sans-serif;
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
        border-radius: 14px;
        margin: 0 auto 32px;
        padding-top: 18px;
        gap: 23px;
    }

    .menu__item {
        margin: 0;
        padding-left: 23px;
    }

    .menu__item:hover {
        text-decoration: underline;
    }

    .menu__item:last-child {
        margin: 900px auto 0;
        text-decoration: none;
        padding-left: 0;
    }
</style>