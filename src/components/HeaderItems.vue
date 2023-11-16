<template>
    <section class="header">
        <div class="header__group-one">
            <img src="../images/logo.svg" class="header__img"/>
            <div class="header__group-two">
                <p class="header__item header__catalog">Каталог</p>
                <div class="header__group-three">
                    <p class="header__item">Оптовые продажи</p>
                    <p class="header__item">Продажи в рознице</p>
                    <p class="header__item">Контакты</p>
                    <p class="header__item">Вакансии</p>
                    <p class="header__item">Отзывы</p>
                </div>
            </div>
        </div>
        <div class="header__button">
            <img class="header__button-img" src="../images/user.svg"/>
            <p class="header__button-text">Личный кабинет</p>
        </div>
    </section>
</template>

<script>
    export default {
        data() {
            return {

            }
        }
    }
</script>

<style>
    @import url('https://fonts.googleapis.com/css2?family=Inter&display=swap');

    .header {
        display: flex;
        width: 100%;
        height: 90px;
        justify-content: space-between;
        align-items: center;
        max-width: 1200px;
        height: 90px;
        margin: 23px auto;
    }

    .header__img {
        width: 120px;
        height: 35px;
    }

    .header__group-one {
        gap: 39px;
        display: flex;
        width: 661px;
        align-items: center;
    }

    .header__group-two {
        display: flex;
        gap: 33px;
    }

    .header__group-three {
        display: flex;
        gap: 20px;
        width: 534px;
        align-items: center;
    }

    .header__item {
        margin: 0;
        font-family: 'Inter', sans-serif;
        font-weight: 500;
        font-size: 14px;
        line-height: 17.5px;
    }

    .header__catalog {
        background-color: #A16341;
        border-radius: 35px;
        width: 120px;
        align-self: center;
        height: 40px;
        display: flex;
        justify-content: center;
        align-items: center;
        border: 1px solid transparent;
        color: #fff;
    }

    .header__catalog:hover {
        border-color: #fac5a9;
    }

    .header__button {
        display: flex;
        justify-content: space-between;
        width: 146px;
        height: 19px;
        border: 1px solid #DBE1ED;
        border-radius: 35px;
        align-items: center;
        padding: 13px 20px;
    }

    .header__button-img {
        width: 24px;
        height: 24px;
    }

    .header__button-text {
        margin: 0;
    }
</style>