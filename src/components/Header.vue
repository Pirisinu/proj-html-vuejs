<script>
import TxtCard from './TxtCard.vue';
export default {
  name: 'Header',
  components: {
    TxtCard
  },
  data(){
    return{
      
    }
  }
}
</script>


<template>
<header>

  <!-- TOP-SIDE -->
  <div class="top">

    <!-- TOP-LEFT-SIDE -->
    <div class="left">
      <img class="logo-header" src="../assets/img/logo-restaurant-2x-300x58.png" alt="">
    </div>

    <!-- TOP-RIGHT-SIDE -->
    <div class="right">
      <ul>
        <li><a href="#">Home</a></li>
        <li><a href="#">Culinary History</a></li>
        <li><a href="#">Our team</a></li>
        <li><a href="#">Our Menu</a></li>
        <li><a href="#">Takeout</a></li>
        <li><a href="#">Bulletin</a></li>
        <li><a href="#">Reservations</a></li>
        <li><a href="#">Home</a></li>
      </ul>
    </div>

  </div>


  <!-- BOTTOM-SIDE -->
  <div class="bottom">

    <!-- BOTTOM-LEFT-SIDE -->
    <div class="left">
      <TxtCard
        :title="'Ciao'"
        :heading="'Ciao4'"
        :description="'Custom Description'"
        :buttonText="'Click Me'"
      >
        <template v-slot:left>
          <p></p>
        </template>
      </TxtCard>


    </div>

    <!-- BOTTOM-RIGHT-SIDE -->
    <div class="right">
      <img class="img-head" src="../assets/img/slider52x.jpg" alt="">
    </div>

  </div>
</header>
</template>

<style lang="scss" scoped>
@use '../scss/partials/colorPalette.scss' as *;
header{
  height: 100vh;
  background-color: $black;
  position: relative;

  //TOP SIDE
  .top{
    height: 120px;
    width: 100%;
    position: absolute;
    top: 0;
    left: 0;
    z-index: 999;
    display: flex; 
    
    .left{
      display: flex;
      align-items: center;

      .logo-header{
        margin-left: 70px;
      }
    }
    .right{
      ul{
        padding: 30px;
        display: flex;
        width: 100%;
        height: 100%;
        justify-content: space-around;
        align-items: center;
      }
    }
  }
  //BOTTOM SIDE
  .bottom{
    display: flex;
    height: 100%;
    .right{
      background-color: cadetblue;
    }
    .left{
      background-color: black;
    }
  }
  .left{
    width: 35%;
    height: 100%;
  }
  .right{
    width: 65%;
    height: 100%;
    position: relative;
    font-size: 1.2rem;
    .img-head{
      object-fit: cover;
      height: 100%;
      width: 100%;
    }
    &::before {
    content: "";
    position: absolute;
    top: 0;
    left: 0;
    width: 100%;
    height: 100%;
    background: linear-gradient(to top, transparent, rgba(0, 0, 0, 0.8));
    z-index: -1;
  }
  }
}
</style>