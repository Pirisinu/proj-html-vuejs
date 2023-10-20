<script>
/* JS */
import mainMenu from '../data/mainMenu.js';
import ltlCard from '../data/mainMenu.js'

/* COMPONENTS */
import LtlCard from './LtlCard.vue';
import TxtCard from './TxtCard.vue';
import MenuCard from './MenuCard.vue';
import NewsPromCard from './NewsPromCard.vue'; 

export default {
  name: 'Main',
  components:{
    TxtCard,
    MenuCard,
    NewsPromCard,
    LtlCard
  },
  data(){
    return{
      mainMenu,
      selectedCard: -1,
      ltlCard
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
  <section class="container food-experience">
    <div class="top">
      <div class="content">
        <p><strong>HAC TELLUS, FELIS RISUS AT</strong> mattis mattis. Eget euismod semper egot tortor, donec amet, blandit. Tristiquen facilisi faucibus elementum feugiat in nam in feugait. Ipsum odio etiam duis facilisis amet vulputate.</p>
        <h3>food is our common ground, a universal experience.</h3>
        <p>Tristique tempus condimentum diam donec. Condimentum Uillamcorper sit elementum hendrerit mi nulla in consequat, ut. Metus, nullam sclerisque netus viverra dui.</p>
        <img class="signature" src="../assets/img/signature-200x172.jpg" alt="">
      </div>
      <div class="img-cont">
        <img src="../assets/img/info22x.jpg" alt="">
      </div>
    </div>

    <div>
      <LtlCard
      v-for='card in ltlCard'
      :key='title'
      :title="'ciao'" 
      :content="'ciao'" 
      :buttonText="'ciao'" 
      />
    </div>
  </section>
  <section class="">img+card</section>
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
  .top{
    display: flex;
    justify-content: space-between;

    .content{
      width: 40%;
      margin: 40px;
      display: flex;
      flex-direction: column;
      justify-content: space-between;
      
      p{}
      h3{
        font-size: 2.5rem;
        text-transform: uppercase;
        font-weight: 600;
        letter-spacing: -1px;
      }
      img.signature{
        height: 80px;
        width: 30%;
      }
    }
    .img-cont{
      height: 600px;
      
      img{
        height: 100%;
        width: 100%;
        object-fit: cover;
      }
    }
  }
}
.card-container{
  display: flex;
  justify-content: center;
  padding: 40px;
}
</style>