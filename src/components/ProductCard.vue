<script>
   
export default {
  props:{
    item: Object
  },

  methods: {

  }
  
}
</script>
<template>
<div class="card">
  
  <div class="card-top">

      <img :src="`/src/assets/img/${item.frontImage}`" :alt="item.name" class="front-img">
      <img :src="`/src/assets/img/${item.backImage}`" :alt="item.name" class="hover-img">
    
  </div>
</div>
</template>


<style lang="scss" scoped>

.card{
width: calc(100% / 3);
padding: 10px 10px;
margin-top: 70px;
.hover-img{
  display: none;
}
}

</style>