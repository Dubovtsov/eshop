<template>
  <div class="v-main-wrapper">
    <h1>{{ title }}</h1>
    <v-catalog></v-catalog>
    <v-cart 
      v-if="CART.length"
      :cart_data="CART"
    >
    
    </v-cart>
  </div>
</template>

<script>
import vCatalog from './v-catalog.vue'
import vCart from './v-cart.vue'
import { mapGetters } from 'vuex'


  export default {
    name: 'v-main-wrapper',
    components: {
      vCatalog,
      vCart,
    },
    props: {},
    data() {
      return {
        title: 'Main'
      }
    },
    computed: {
      ...mapGetters([
        'CART'
      ])
    },
    method: {},
    wath: {},
    mounted() {},
  }
</script>

<style scoped>
.v-main-wrapper {
  max-width: 900px;
  margin: 0 auto;
}
</style>
