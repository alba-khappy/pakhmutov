<template lang='pug'>
div
  HeaderComponent
  main.container
    ul.product__list 
      ProductItem(
                  v-for="product in productList",
                  :img ="product.img",
                  :content ="product.content"
              )
  FooterComponent

</template>

<script>
import HeaderComponent from './components/HeaderComponent.vue';
import ProductItem from './components/ProductItem.vue';
import FooterComponent from './components/FooterComponent.vue';


export default {
  name: 'App',
  components: {
    HeaderComponent,
    ProductItem,
    FooterComponent
},
   data (){
        return {
            
            productList: [
                {
                    img: "book1.jpg",
                    content: "Отечественная бонистика",
                },
                {
                    img: "book2.jpeg",
                    content: "Позитивные изменения №2-2022",
                },
                {
                    img: "book1.jpg",
                    content: "Вестник ЮНЕСКО №48",
                },
                {
                    img: "book2.jpeg",
                    content: "Аукцион №32 «Коллекционные монеты и медали»",
                },
                {
                    img: "book1.jpg",
                    content: "Отечественная бонистика",
                },
                {
                    img: "book2.jpeg",
                    content: "Позитивные изменения №2-2022",
                },
                {
                    img: "book1.jpg",
                    content: "Вестник ЮНЕСКО №48",
                },
                {
                    img: "book2.jpeg",
                    content: "Аукцион №32 «Коллекционные монеты и медали»",
                },
                ]}
            },
}
</script>

<style lang="scss">
    @import "./assets/scss/general.scss";


#app {
  font-family: Arial, Helvetica, sans-serif;
  -webkit-font-smoothing: antialiased;
  -moz-osx-font-smoothing: grayscale;
}

.product__list {
  display: flex;
  flex-wrap: wrap;
  justify-content: flex-start;
  border-bottom: 1px solid #666;
  margin-bottom: 20px;
}

@media (max-width: 830px) {
  .product__list {
    justify-content: center;
  }
}

</style>
