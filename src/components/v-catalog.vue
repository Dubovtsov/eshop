<template>
  <div class="v-catalog">
    <h1>Catalog</h1>
    <div class="v-catalog__list">
      <v-catalog-item 
        v-for="product in products"
        :key="product.article"
        :product_data="product"
        @sendArticle="showChildArticleInConsole"
      >
      </v-catalog-item>
    </div>
  </div>
</template>

<script>
import vCatalogItem from './v-catalog-item'
  export default {
    name: 'v-catalog',
    components: {
      vCatalogItem
    },
    data() {
      return {
        products: [
          {
            image: "1.jpg",
            name: "Name 1",
            price: 100,
            article: "dep1",
            available: true
          },
          {
            image: "2.jpg",
            name: "Name 2",
            price: 200,
            article: "dep2",
            available: true
          },
          {
            image: "3.jpg",
            name: "Name 3",
            price: 100,
            article: "dep3",
            available: true
          },
          {
            image: "4.jpg",
            name: "Name 4",
            price: 100,
            article: "dep4",
            available: true
          },
          {
            image: "5.jpg",
            name: "Name 5",
            price: 100,
            article: "dep5",
            available: true
          },
          {
            image: "6.jpg",
            name: "Name 6",
            price: 100,
            article: "dep6",
            available: true
          }
        ]
      }
    },
    methods: {
      showChildArticleInConsole(data) {
        console.log(data)
      }
    }
  }
</script>

<style lang="scss">
  .v-catalog {
    &__list {
      display: flex;
      flex-wrap: wrap;
      justify-content: space-between;
      align-items: center;
    }
  }
</style>