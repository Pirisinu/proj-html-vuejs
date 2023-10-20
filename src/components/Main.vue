<script>
import mainMenu from '../data/mainMenu.js';
import TxtCard from './TxtCard.vue';
import MenuCard from './MenuCard.vue';
import NewsPromCard from './NewsPromCard.vue'; 

export default {
  name: 'Main',
  components:{
    TxtCard,
    MenuCard,
    NewsPromCard
  },
  data(){
    return{
      mainMenu
    }
  },
  mounted(){
    console.log(mainMenu[0]);
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
  </section>
  <section class="">img+card</section> -->
  <section>
    <MenuCard 
      v-for="(menu, index) in mainMenu"
      :key="index"
      :menu='menu'
    />
  </section>

</template>

<style lang="scss" scoped>
@use '../scss/main.scss' as *;

.food-experience{

  img{

  }
}

</style>