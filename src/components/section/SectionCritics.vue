<script>
import CriticsCard from '../card/CriticsCard.vue';
export default {
  name: 'SectionCritics',
  components:{
    CriticsCard
  }
}
</script>

<template>
  <h2>What critics are saying about us</h2>
  <div class="line"></div>
  <div class="container-card">
    <div class="big-card">
      <img src="/discover-menu.jpg" alt="">
      <CriticsCard 
      class="right"
      :name="'Meggy stewart'"
      :heading="'New york times'"
      :description="'lorem ipsum dolor sit amet, consectetur adipiscing elit, sed do eiusmod tempor incididunt ut labore et dolore magna aliqua et dolore magna aliqua et dolore magna al Lorem ipsum dolor sit amet, consect et aL S'"
      :buttonText="'Read full article'"
      />
    </div>
    <div class="container-ltl-card">
      <CriticsCard 
      class="ltl-card mary"
      :name="'mary maxey'"
      :heading="'the guardian'"
      :description="'lorem ipsum dolor sit amet, consectetur adipiscing elit, sed do eiusmod tempor incididunt ut labore et dolore magna aliqua et dolore magna aliqua et dolore magna al Lorem ipsum dolor sit amet, consect et aL S'"
      :buttonText="'Read full article'"
      />
      <CriticsCard 
      class="ltl-card patrick"
      :name="'patrick monroe'"
      :heading="'globe and mail'"
      :description="'lorem ipsum dolor sit amet, consectetur adipiscing elit, sed do eiusmod tempor incididunt ut labore et dolore magna aliqua et dolore magna aliqua et dolore magna al Lorem ipsum dolor sit amet, consect et aL S'"
      :buttonText="'Read full article'"
      />
    </div>
  </div>
</template>

<style lang="scss" scoped>
h2{
  text-align: center;
  font-style: oblique;
  font-weight: 500;
  font-size: 2.2rem;
  margin-top: 60px;
}
.line{
  margin: 20px auto;
}
.container-card{
  width: 70%;
  margin: 0 auto;
  display: flex;
  flex-wrap: wrap;
  .big-card{
    width: 100%;
    display: flex;
    .right{
      width: 100%;
      background-color: black;
    }
  }
  .container-ltl-card{
    display: flex;
    justify-content: space-between;
    width: 100%;
    .ltl-card{ 
      width: 45%;
      margin: 60px 0;
      /* card effect */
      border-radius: 120px 160px 90px 220px;
    }
    .ltl-card.mary{
      height: 550px;
      background: linear-gradient(rgba(0, 0, 0), rgba(0, 0, 0, 0.3)), url('/info52x.jpg');
      background-size: cover;
      background-position: center;
    }
    .ltl-card.patrick{

      height: 550px;
      background: linear-gradient(rgba(0, 0, 0), rgba(0, 0, 0, 0.3)), url('/info12x.jpg');
      background-size: cover;
      background-position: center;
    }
  }
}
</style>