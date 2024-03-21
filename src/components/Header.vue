<script>
  export default {
    
  }
</script>

<template>

  <header>
    <div class="container menu">
      <ul>
        <li><a href="#">Donna</a></li>
        <li><a href="#">Uomo</a></li>
        <li><a href="#">Bambini</a></li>
      </ul>

      <div class="logo">
        <img src="../assets/img/boolean-logo.png" alt="">
      </div>

      <div class="icons">
        <i class="fa-regular fa-user"></i>  
        <i class="fa-regular fa-heart"></i>  
        <i class="fa-solid fa-cart-shopping"></i> 
       </div>
    </div>
  </header>
  
</template>


<style lang="scss" scoped>

@use '../assets/scss/partials/variables' as *;

header{
  background-color: $bg-header;
  display: flex;
  justify-content: space-between;
  ul{
    list-style: none;
    display: flex;     
    li{
      a{
        text-decoration: none;
        color: $link-color;
        font-weight: bold;
        padding: 0px 5px;
      }
    }
  }
  img{
    width: 100px;
  }
}

.menu{
  display: flex;
  justify-content: space-between;
  padding: 20px; 
  .icons{
    color: $link-color;
    i{
      padding: 0px 10px;
    }
  }
}

</style>