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
      mainMenu,
      selectedCard: -1,
    }
  },
  mounted(){
    console.log(mainMenu[0]);
  },
  methods: {
    selectCard(index) {
      this.mainMenu.forEach((menu, i) => {
        menu.isSelected = i === index;
      });
    },
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
  <section class="card-container">
    <MenuCard
      v-for="(menu, index) in mainMenu"
      :key="index"
      :menu='menu'
      :isSelected="menu.isSelected"
      @clickCard="selectCard(index, $event)"

    />
  </section>

</template>

<style lang="scss" scoped>
@use '../scss/main.scss' as *;

.food-experience{

  img{

  }
}
.card-container{
  display: flex;
  justify-content: center;
  padding: 40px;
}
</style>