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

</template>

<script>
import HeaderComponent from './components/HeaderComponent.vue';
import ProductItem from './components/ProductItem.vue';


export default {
  name: 'App',
  components: {
    HeaderComponent,
    ProductItem
  },
   data (){
        return {
            productList: [
                {
                    img: "book1.jpg",
                    content: "Отечественная бонистика",
                },
                {
                    img: "book1.jpg",
                    content: "Позитивные изменения №2-2022",
                },
                {
                    img: "book1.jpg",
                    content: "Вестник ЮНЕСКО №48",
                },
                {
                    img: "book1.jpg",
                    content: "Аукцион №32 «Коллекционные монеты и медали»",
                },
                ]}
            },
}
</script>

<style lang="scss">
    @import "./assets/scss/general.scss";


#app {
  font-family: Avenir, Helvetica, Arial, sans-serif;
  -webkit-font-smoothing: antialiased;
  -moz-osx-font-smoothing: grayscale;
  text-align: center;
  color: #2c3e50;
  margin-top: 60px;
}

.product__list {
  display: flex;
  flex-wrap: wrap;
  justify-content: space-between;
}
</style>
