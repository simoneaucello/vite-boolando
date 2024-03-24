<script>
   
export default {
  props:{
    item: Object
  },

  methods: {
    getDiscountPrice() {
      let discountPrice;
      this.item.badges.forEach((item) => {
        if (item.type === "discount") {
          discountPrice = this.item.price - this.item.price * Math.abs(parseFloat(item.value) / 100);
        }
      });
      return discountPrice ? discountPrice.toFixed(2) : null;
    },
  }  
}
</script>

<template>
<div class="card">
  
  <div class="card-top">

      <img :src="`/src/assets/img/${item.frontImage}`" :alt="item.name" class="front-img">
      <img :src="`/src/assets/img/${item.backImage}`" :alt="item.name" class="hover-img">

      <div class="wishlist" :class="{ 'favourite': item.isInFavorites }">&hearts;</div>
      <div class="badges">
        <span
          v-for="(badge, index) in item.badges"
          :key="index"
          :class="badge.type">{{ badge.value }}</span>
      </div>   
  </div>

  <div class="bottom-card">
      <div class="brand">{{ item.brand }}</div>
      <div class="product">{{ item.name }}</div>
      <div>
        <span v-if="getDiscountPrice()" class="sale-price">{{ getDiscountPrice() }} &euro;</span>
        <span :class="{ 'previous' : getDiscountPrice() }">{{ item.price }} &euro;</span> 
      </div>
  </div>

</div>
</template>


<style lang="scss" scoped>
@use "../assets/scss/partials/variables" as *;

.card{
  width: calc(100% / 3.2);
  margin: 10px;
  margin-top: 70px;
  background-color: #fff;
  .card-top{
    position: relative;
  }

  .hover-img{
    display: none;
  }
  
  .wishlist {
    background-color: $color-white;
    font-size: $font-large;
    padding: 5px 12px;
    position: absolute;
    right: 0;
    top: 2%;

    &:hover {
      color: $favourite;
    }
}
  .badges{
    position: absolute;
    font-weight: bold;
    bottom: 8%;
    color: $color-white;
    font-size: $font-m;
      .discount,
      .tag {
        padding: 5px 15px;
      }

      .discount {
        background-color: $color-discount;
      }

      .tag {
        background-color: $color-value;
      }
  }

  .favourite{
    color: $favourite;
  }

  .bottom-card {
    font-size: $font-m;
    text-align: start;
    margin-left: 10px;
    padding: 10px;

    .product {
      font-weight: bold;
      text-transform: uppercase;
      font-size: $font-m;
    }

    .sale-price {
      color: $color-discount;
      font-weight: bold;
    }

    .previous {
      text-decoration: line-through;
    }
  }

  &:hover{
    .hover-img{
      display: block;
    }
    .front-img{
      display: none;
    }
  }
}

</style>