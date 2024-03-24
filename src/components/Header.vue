<script>
import { headerMenues } from '../data/menues';
  export default {

    computed: {
      mainMenu(){
        return headerMenues.main
      }    ,
      socialMenu(){
        return headerMenues.social
      }  
    },

    mounted(){

    }
    
  }
</script>

<template>

  <header>
    <div class="container menu">
      <ul>
        <li v-for="(item, index) in mainMenu"
        :key='`h-${index}`'><a :href="item.href">{{item.text}}</a></li>
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
  position: fixed;
  left: 0;
  right: 0;
  z-index: 99;
  background-color: $bg-header;
  box-shadow: 1px 1px 15px rgb(92, 92, 92);
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
      &:hover{
        text-decoration: underline;;
      }
    }
}

</style>