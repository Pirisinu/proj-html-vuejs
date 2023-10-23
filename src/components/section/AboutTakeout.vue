<script>
import TxtCard from '../card/TxtCard.vue';
export default {
  name: 'AboutTakeout',
  components:{
    TxtCard
  }
}
</script>

<template>
  <section class="about takeout">
    <div class="left img-box">
      <img src="../../assets/img/slider72x-scaled.jpg" alt="img cibo">
    </div>
    <div class="right">
      <TxtCard
      class="white-card"
        :title="'enjoy your meal at home'"
        :heading="'takeout now available'"
        :description="`Pellentesque vitae viverra risus, sagittis. venenatis ridiculus sclerisque nisi urna nulla. Sit tempor a et nisl, ac felis.`"
        :buttonText="'view takeout menu'"
      >
        <template v-slot:left>
          <span class="line"></span>
        </template>
      </TxtCard>
    </div>
  </section>
</template>

<style lang="scss" scoped>
@use '../../scss/main.scss' as *;
section.about{
  display: flex;
  height: 850px;
  .left{
    width: 55%;
    img{
      object-fit: cover;
    }
  }
  .right{
    padding: 60px;
    width: 45%;
    background-color: $black;
  }
  .line{
    margin-top: 15px;
    margin-right: 10px;
  }
}

</style>