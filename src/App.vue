<template>
    <HeaderItems />
    <div class="page-content">
      <CarouselItems />
      <div class="content">
        <MenuItems />
        <div style="background: #333; width: 100%;">sdadf</div>
      </div>
    </div>
    <FooterItems />
</template>

<script>
    import HeaderItems from './components/HeaderItems.vue';
    import FooterItems from './components/FooterItems.vue';
    import CarouselItems from './components/CarouselItems.vue';
    import MenuItems from './components/MenuItems.vue';

    export default {
        components: {
            HeaderItems,
            FooterItems,
            CarouselItems,
            MenuItems,
}
    }
</script>

<style>
  @import url('https://fonts.googleapis.com/css2?family=Inter&display=swap');

  .page-content {
    min-height: 200px;
  }

  .content {
    max-width: 1200px;
    width: 100%;
    margin: 31px auto 45px;
    display: flex;
    flex-direction: row;
    gap: 20px;
    justify-content: space-between;
  }

  #app {
    overflow-x: hidden;
  }

  body {
    background-color: #f3f3f3;
    font-family: Inter;
  }

</style>
