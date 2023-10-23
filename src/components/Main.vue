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
  <!-- SECTION EXPERIENCE -->
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

    <div class="bottom">
      <LtlCard/>
    </div>
  </section>
  
  <!-- SECTION ABOUT -->
  <section class="about">
    <div class="left img-box">
      <img src="../assets/img/slider32x.jpg" alt="img cibo">
    </div>
    <div class="right">
      <TxtCard
      class="white-card"
        :title="'fine dining experience'"
        :heading="'the best table in town'"
        :description="`Pellentesque vitae viverra risus, sagittis. venenatis ridiculus sclerisque nisi urna nulla. Sit tempor a et nisl, ac felis.`"
        :buttonText="'Explore the menu'"
      >
        <template v-slot:left>
          <span class="line"></span>
        </template>
      </TxtCard>
    </div>
  </section>

  <!-- SECTION ABOUT -->
  <section class="about">
    <div class="left img-box">
      <img src="../assets/img/slider72x-scaled.jpg" alt="img cibo">
    </div>
    <div class="right">
      <TxtCard
      class="white-card"
        :title="'enjoy your meal at home'"
        :heading="'takeout now available'"
        :description="`Pellentesque vitae viverra risus, sagittis. venenatis ridiculus sclerisque nisi urna nulla. Sit tempor a et nisl, ac felis.`"
        :buttonText="'Explore the menu'"
      >
        <template v-slot:left>
          <span class="line"></span>
        </template>
      </TxtCard>
    </div>
  </section>

  <!-- SECTION MENU -->
  <section class="menu-card-container">
    <MenuCard
      v-for="(menu, index) in mainMenu"
      :key="index"
      :menu='menu'
      :isSelected="menu.isSelected"
      @clickCard="selectCard(index, $event)"

    />
  </section>

  <section>
    
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
  .bottom{
    margin-top: 80px;
  }
}
.about{
  display: flex;
  height: 850px;
  .left{
    width: 55%;
    img{
      object-fit: cover;
    }
  }
  .right{
    width: 45%;
    background-color: $black;
  }
}
.menu-card-container{
  display: flex;
  justify-content: center;
  padding: 40px;
}
</style>