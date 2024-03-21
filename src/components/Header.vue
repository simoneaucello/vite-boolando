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

      <div >
        <a href="#"><i class="fa-regular fa-user"></i></a>
        <a href="#"><i class="fa-regular fa-heart"></i></a>
        <a href="#"><i class="fa-solid fa-cart-shopping"></i> </a>       
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
    a{
      padding: 0px 10px;
      color: $link-color;
    }
}

</style>