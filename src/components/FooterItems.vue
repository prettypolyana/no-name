<template>
    <section class="footer">
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
    </section>
</template>

<script>
    export default {

    }
</script>

<style>
    .footer {
        background-color: black;
        width: 1200px;
        height: 16px;
        color: rgb(172, 172, 172);
        position: absolute;
        bottom: 0;
        display: flex;
        padding: 29px 120px;
        gap: 400px;
    }

    .footer__text {
        margin: 0;
    }

    .footer__link {
        text-decoration: underline;
    }

    .footer__one {
        display: flex;
        gap: 31px;
    }
</style>