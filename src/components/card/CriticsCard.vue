<script>
export default {
  name: 'CriticsCard',
  props:{
    imageSrc: String,
    title: String,
    ltlPrice: String,
    heading: String,
    description: String,
    buttonText: String
  }
}
</script>


<template>
  <div class="card-box">
    <div class="card">
      <h3 class="title">{{ title }}</h3>
      <span><i class="fa-solid fa-star"></i></span>
      <h1 class="heading">{{ heading }}</h1>
      <p class="description">{{ description }}</p>
      <button @click="buttonClick">{{ buttonText }}</button>
    </div>
  </div>

</template>

<style>

</style>