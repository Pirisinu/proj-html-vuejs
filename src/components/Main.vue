<script>
/* JS */
import mainMenu from '../data/mainMenu.js';
import ltlCard from '../data/mainMenu.js'

/* COMPONENTS */
/* CARD IMPORT */
import TxtCard from './card/TxtCard.vue';
import LtlCard from './card/LtlCard.vue';
import MenuCard from './MenuCard.vue';
import NewsPromCard from './card/NewsPromCard.vue';
import CriticsCard from './card/CriticsCard.vue';
/* SECTION IMPORT */
import SectionFoodExperience from './section/SectionFoodExperience.vue';
import SectionAboutMenu from './section/AboutMenu.vue';
import SectionCritics from './section/SectionCritics.vue';
import SectionPlateImg from './section/SectionPlateImg.vue';
import SectionAboutTakeout from './section/AboutTakeout.vue';
import SectionNewsProm from './section/SectionNewsProm.vue';
import SectionPlateSlider from './section/SectionPlateSlider.vue';

export default {
  name: 'Main',
  components:{
    /* CARD */
    TxtCard,
    MenuCard,
    NewsPromCard,
    LtlCard,
    CriticsCard,
    /* SECTION */
    SectionFoodExperience,
    SectionAboutMenu,
    SectionCritics,
    SectionPlateImg,
    SectionAboutTakeout,
    SectionNewsProm,
    SectionPlateSlider
  },
  data(){
    return{
      mainMenu,
      ltlCard
    }
  },
  methods: {
    /* Metodo per far girare lo slider in <SectionPlateSlider /> */
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
  <SectionFoodExperience />
  <!-- SECTION ABOUT MENU -->
  <SectionAboutMenu />
  <!-- SECTION CRITICS -->
  <SectionCritics />
  <!-- SECTION IMG PLATE -->
  <SectionPlateImg />
  <!-- SECTION NEWS PROM -->
  <section>
    <h2>Latest news & promotions</h2>
    <div class="line"></div>

    <div class="news-prom">
      <NewsPromCard 
      :imageSrc="'/img-caffe.jpg'"
      :title="'the best coffee in town'"
      :description="'by admin  January 7th, 2020  Categories: News'"
      />
      <NewsPromCard 
      :imageSrc="'/discover-menu.jpg'"
      :title="'discover our new menu'"
      :description="'by admin  January 7th, 2020  Categories: News'"
      />
      <NewsPromCard 
      :imageSrc="'/pay.jpg'"
      :title="'we now accept square!'"
      :description="'by admin  January 7th, 2020  Categories: News'"
      />
    </div>
  </section>

  <!-- SECTION ABOUT TAKEOUT -->
  <SectionAboutTakeout />

  <!-- SECTION MENU -->
  <section class="menu-card-container">
    <MenuCard
      v-for="(menu, index) in mainMenu"
      :key="index"
      :menu='menu'
      :isSelected="menu.isSelected"
      @clickCard="selectCard(index)"

    />
  </section>

  <!-- SECTION PLATE SLIDER -->
  <SectionPlateSlider />
</template>

<style lang="scss" scoped>
@use '../scss/main.scss' as *;

/* NEWS-PROM */
section {
  padding: 50px 0px;
  h2{
    text-align: center;
    font-weight: 500;
    font-size: 2rem;
    padding-top: 50px;
  }
  .line{
    margin: 50px auto 0px;
  }
  .news-prom{
  display: flex;
  padding: 0px 250px;
  margin: 100px 0px;
  }
}
section.menu-card-container{
  display: flex;
  justify-content: center;
  margin: 100px 0px;
  padding: 40px;
}
</style>