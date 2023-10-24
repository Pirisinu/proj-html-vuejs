<script>
import TxtCard from '../card/TxtCard.vue';
export default {
  name: 'SectionAboutMenu',
  components:{
    TxtCard
  }
}
</script>

<template>
  <section class="about">
    <div class="left img-box">
      <img src="../../assets/img/slider32x.jpg" alt="img cibo">
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