<script>
import ltlCardData from '../data/ltlCard.js'; 

export default {
  name: 'LtlCard',
  data() {
    return {
      ltlCard: ltlCardData
    }
  }
}
</script>

<template>
  <div class="card-box">
    <div v-for="(card, index) in ltlCard" :key="index" class="card">
      <img class="ltl-img" :src="card.imageSrc" :alt="card.imageAlt" />
      <h4>{{ card.title }}</h4>
      <span class="line"></span>
      <p>{{ card.content }}</p>
      <button class="light-button">{{ card.buttonText }}</button>
    </div>
  </div>
</template>



<style lang="scss" scoped>
.card-box{
  display: flex;
  .card{
    text-align: center;
    display: flex;
    flex-direction: column;
    justify-content: space-between;
    height: 300px;
    padding: 0px 40px;
    .line{
      margin: 0 auto;
    }
    .ltl-img{
      height: 80px;
      width: 80px;
      object-fit: contain;
      margin: 0 auto;
    }
  }
}
</style>