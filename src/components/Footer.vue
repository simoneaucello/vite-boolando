<script>
  export default {
    computed: {
      socialMenu(){
        return footerMenues.social;
      },   
  }
}
</script>

<template>

  <footer>
    <div class="container bot-menu">
      <div class="col">
        <h4>Boolando s.r.l</h4>
        <ul>
          <li><a href="#">Informazioni legali</a></li>
          <li><a href="#">Informazioni sulla privacy</a></li>
          <li><a href="#">Diritto di recesso</a></li>
        </ul>
      </div>
      <div class="col">
        <h4>Trovaci anche su</h4>

        <a href="#"><i class="fa-brands fa-x-twitter"></i></a>
        <a href="#"><i class="fa-brands fa-square-facebook"></i></a>
        <a href="#"><i class="fa-brands fa-square-instagram"></i></a>
        <a href="#"><i class="fa-brands fa-square-pinterest"></i></a>
        <a href="#"><i class="fa-brands fa-square-youtube"></i></a>

        
      </div>
    </div>
  </footer>
  
</template>


<style lang="scss" scoped>

@use '../assets/scss/partials/variables' as *;

footer{
  background-color: $bg-footer;
  color: $primary-color;
  .bot-menu{
    display: flex;
    justify-content: space-between;
    padding: 30px;
    ul{
      display: flex;
      list-style: none;
      li{
        padding: 10px 5px;
        a{
          color: $link-color;
          text-decoration: none;
        }
      }
    }
  }
  h4{
    padding: 5px;
  }
  a{
    color: $link-color;
    i{
      padding: 10px 5px;
    }
  }
    
}

</style>