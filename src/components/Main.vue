<script>
import ProductCard from './ProductCard.vue';
import {products} from '../data/db.json'
  export default {
    components:{
      ProductCard
    },
    data(){
      return {
        products
      }
    },
    
  }
</script>

<template>

  <main>
    <div class="container flexed">
      <ProductCard 
        v-for="product in this.products"
        :key="product.id"
        :item="product"
      />

    </div>
  </main>
  
</template>


<style lang="scss" scoped>
@use '../assets/scss/partials/variables' as *;


main{
  text-align: center;
  display: flex;
  justify-content: center;
  align-items: center;
  padding: 30px 0;
  background-color: $bg-main;
}

</style>