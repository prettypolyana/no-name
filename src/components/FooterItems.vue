<template>
    <section class="footer">
        <div class="footer__content">
            <p class="footer__text">
                © Кондитерские изделия «Кристалл», 2000–2024
            </p>
            <div class="footer__one">
                <a class="footer__text footer__link">
                    Политика конфиденциальности
                </a>
                <p class="footer__text">
                    +7 (8412) 709-900
                </p>
            </div>
        </div>
    </section>
</template>

<script>
    export default {

    }
</script>

<style>
    .footer {
        background-color: black;
        width: 100%;
        height: 16px;
        color: rgb(172, 172, 172);
        padding: 29px 0;
    }

    .footer__content {
        width: 100%;
        max-width: 1200px;
        margin: 0 auto;
        display: flex;
        justify-content: space-between;
    }

    .footer__text {
        margin: 0;
    }

    .footer__link {
        text-decoration: underline;
    }

    .footer__one {
        display: flex;
        gap: 30px;
    }
</style>