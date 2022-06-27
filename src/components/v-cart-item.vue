<template>
    <div class="v-cart-item">
      <div class="v-cart-item__info">
        <p>{{cart_item_data.name}}</p>
        <p>{{cart_item_data.price}}</p>
        <p>{{cart_item_data.article}}</p>
      </div>     
      <div class="v-cart-item__quantity"></div>
      <button class="btn">Delete</button>
    </div>
</template>

<script>

  export default {
    name: "v-cart-item",
   
    props: {
      cart_item_data: {
        type: Object,
        default() {
          return {}
        }
      }
    },
    data() {
      return {}
    },
    methods: {
      addQuantity() {
        this.cart_item_data.quantity = 1
      }
    },
    computed: {},
    mounted() {
     addQuantity()
    }
  }
</script>

<style lang="scss">
  .v-cart-item {
    display: flex;
    justify-content: space-between;
    flex-wrap: nowrap;
    align-content: center;
    
    border-radius: 0.5em;
    background: #e0e0e0;
    box-shadow:  6px 6px 12px #bebebe,
                -6px -6px 12px #ffffff;
    padding: $padding*2;
    margin-bottom: $margin*2;
  
  }
</style>