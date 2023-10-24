<script>
import NewsPromCard from '../card/NewsPromCard.vue';
export default {
  name: 'SectionNewsProm',
  components:{
    NewsPromCard
  }
}
</script>

<template>
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
</template>

<style lang="scss" scoped>
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
</style>