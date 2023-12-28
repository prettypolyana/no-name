<template>
    <div class="catalog">
      <div class="catalog__page">
        <div class="catalog__texts">
          <p class="catalog__title">Каталог</p>
          <select v-model="selected" class="catalog__select">
            <option class="catalog__option" value="asc">Сначала дешевле</option>
            <option class="catalog__option" value="desc">Сначала дороже</option>
          </select>
        </div>
        <CatalogMenu :items="sortedItems"/>
      </div>
    </div>
  </template>
  
  <script>
  import CatalogMenu from './CatalogMenu.vue';
  
  export default {
    data() {
      return {
        selected: 'asc',

        items: [
                    {id: 1, path: "cake-1.png", weigh: "200gr", kcal: "250 ккал", name: "Тортик", price: "200 ₽", text: "Ну очень вкусная штука)"},
                    {id: 2, path: "cake-2.png", weigh: "200gr", kcal: "250 ккал", name: "Тортик", price: "100 ₽", text: "Ну очень вкусная штука)"},
                    {id: 3, path: "cake-3.png", weigh: "200gr", kcal: "250 ккал", name: "Тортик", price: "300 ₽", text: "Ну очень вкусная штука)"},
                    {id: 4, path: "cake-1.png", weigh: "200gr", kcal: "250 ккал", name: "Тортик", price: "200 ₽", text: "Ну очень вкусная штука)"},
                    {id: 5, path: "cake-2.png", weigh: "200gr", kcal: "250 ккал", name: "Тортик", price: "100 ₽", text: "Ну очень вкусная штука)"},
                    {id: 6, path: "cake-3.png", weigh: "200gr", kcal: "250 ккал", name: "Тортик", price: "300 ₽", text: "Ну очень вкусная штука)"},
                    {id: 7, path: "cake-1.png", weigh: "200gr", kcal: "250 ккал", name: "Тортик", price: "200 ₽", text: "Ну очень вкусная штука)"},
                    {id: 8, path: "cake-2.png", weigh: "200gr", kcal: "250 ккал", name: "Тортик", price: "100 ₽", text: "Ну очень вкусная штука)"},
                    {id: 9, path: "cake-3.png", weigh: "200gr", kcal: "250 ккал", name: "Тортик", price: "300 ₽", text: "Ну очень вкусная штука)"},
                    {id: 10, path: "cake-1.png", weigh: "200gr", kcal: "250 ккал", name: "Тортик", price: "200 ₽", text: "Ну очень вкусная штука)"},
                    {id: 11, path: "cake-2.png", weigh: "200gr", kcal: "250 ккал", name: "Тортик", price: "100 ₽", text: "Ну очень вкусная штука)"},
                    {id: 12, path: "cake-3.png", weigh: "200gr", kcal: "250 ккал", name: "Тортик", price: "300 ₽", text: "Ну очень вкусная штука)"},
                    {id: 13, path: "cake-1.png", weigh: "200gr", kcal: "250 ккал", name: "Тортик", price: "200 ₽", text: "Ну очень вкусная штука)"},
                    {id: 14, path: "cake-2.png", weigh: "200gr", kcal: "250 ккал", name: "Тортик", price: "100 ₽", text: "Ну очень вкусная штука)"},
                    {id: 15, path: "cake-3.png", weigh: "200gr", kcal: "250 ккал", name: "Тортик", price: "300 ₽", text: "Ну очень вкусная штука)"},
                    {id: 16, path: "cake-1.png", weigh: "200gr", kcal: "250 ккал", name: "Тортик", price: "200 ₽", text: "Ну очень вкусная штука)"},
                    {id: 17, path: "cake-2.png", weigh: "200gr", kcal: "250 ккал", name: "Тортик", price: "100 ₽", text: "Ну очень вкусная штука)"},
                    {id: 18, path: "cake-3.png", weigh: "200gr", kcal: "250 ккал", name: "Тортик", price: "300 ₽", text: "Ну очень вкусная штука)"},
                    {id: 19, path: "cake-1.png", weigh: "200gr", kcal: "250 ккал", name: "Тортик", price: "200 ₽", text: "Ну очень вкусная штука)"},
                    {id: 20, path: "cake-2.png", weigh: "200gr", kcal: "250 ккал", name: "Тортик", price: "100 ₽", text: "Ну очень вкусная штука)"},
        ],
      };
    },
    components: { CatalogMenu },
    computed: {
      sortedItems() {
        let sortedArray = this.items;
        if (this.selected === 'asc') {
            sortedArray = sortedArray.sort((a, b) => Number.parseInt(a.price) - Number.parseInt(b.price));
        } else if (this.selected === 'desc') {
            sortedArray = sortedArray.sort((a, b) => Number.parseInt(b.price) - Number.parseInt(a.price));
        }
        return sortedArray;
      },
    },
  };
  </script>
  

<style>
    @import url('https://fonts.googleapis.com/css2?family=Playfair+Display:wght@800&display=swap');

    .catalog {
        width: 895px;
        height: 1710px;
        background-color: #fff;
        border-radius: 16px;
    }

    .catalog__page {
        margin: 29px 30px 0;
    }

    .catalog__texts {
        display: flex;
        justify-content: space-between;
    }

    .catalog__title {
        font-family: 'Playfair Display', sans-serif;
        font-size: 22px;
        font-weight: 800;
        line-height: 22px;
        margin: 0;
    }

    .catalog__select {
        border: none;
        outline: none;
        font-family: 'Inter', sans-serif;
        font-size: 14px;
        font-weight: 500;
        line-height: 18px;
        text-align: center;
        color: #97A1B0;
    }
</style>