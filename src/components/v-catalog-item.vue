<template>
  <div class="v-catalog-item">
    <h1 class="v-catalog-item__name">{{product_data.name}}</h1>
    <p class="v-catalog-item__price">Price: {{product_data.price}}$</p>
    <button 
      class="v-catalog-item__add_to_cart_btn btn" 
      @click="addToCart"
      >Add to cart
    </button>
  </div>
</template>

<style lang="scss">
  .v-catalog-item {
    flex-basis: 25%;
    // box-shadow: 0 0 8px 0 #e0e0e0;
    border-radius: 0.5em;
    background: #e0e0e0;
    box-shadow:  6px 6px 12px #bebebe,
                -6px -6px 12px #ffffff;
    padding: $padding*2;
    margin-bottom: $margin*2;
  }
</style>

<script>
export default {
  name: "v-catalog-item",
  props: {
    product_data: {
      type: Object,
      default() {
        return {}
      }
    }
  },
  methods: {
    addToCart() {
      this.$emit('addToCart', this.product_data)
    }
  }
}
</script>