<script>
export default {
  name: 'CriticsCard',
  props:{
    name: String,
    heading: String,
    description: String,
    buttonText: String
  }
}
</script>


<template>
  <div class="card-box">
    <div class="card">
      <span class="name">{{ name }}</span>
      <h1 class="heading">{{ heading }}</h1>
      <span class="star-container">
        <i class="fa-solid fa-star"></i><i class="fa-solid fa-star"></i><i class="fa-solid fa-star"></i><i class="fa-solid fa-star"></i><i class="fa-solid fa-star"></i>
      </span>
      <div class="line"></div>
      <p class="description">{{ description }}</p>
      <button @click="buttonClick">{{ buttonText }}</button>
    </div>
  </div>

</template>

<style lang="scss" scoped>
  .card-box{
    color: white;
    
  }
</style>