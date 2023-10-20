<script>
import TxtCard from './TxtCard.vue';
import mainMenu from '../data/mainMenu.js';
import MenuCard from './MenuCard.vue';
import CriticsCard from './CriticsCard.vue'; 

export default {
  name: 'Main',
  components:{
    TxtCard,
    MenuCard,
    CriticsCard
  },
  data(){
    return{
      mainMenu
    }
  },
  mounted(){
    console.log(mainMenu);
  }
}
</script>


<template>
  <!-- <section class="container food-experience">
    <div>
      <div></div>
      <div>
        <img src="../assets/img/info22x.jpg" alt="">
      </div>
    </div>
    <div></div>
  </section> -->
  <section class="">img+card</section>
  <section>

  </section>

</template>

<style lang="scss" scoped>
@use '../scss/main.scss' as *;

.food-experience{

  img{

  }
}

</style>