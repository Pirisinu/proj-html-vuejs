<script>
export default {
  name: 'NewsPromCard',
  props:{
    imageSrc: String,
    title: String,
    description: String
  }
}
</script>


<template>
  <div class="card wavy-border-div">
    <img :src="imageSrc" alt="Card Image" v-if="imageSrc" />
    <h3 class="title">{{ title }}</h3>
    <p class="description">{{ description }}</p>
  </div>
</template>

<style lang="scss" scoped>
.card{
  height: 550px;
  width: calc(100% / 3 - 40px);
  margin: 0px 40px;
  background-color: black;
  text-align: center;

  img{
    object-fit: cover;
  }
}

</style>