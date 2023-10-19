<script>
export default {
  name: 'TxtCard',
  props:{
    imageSrc: String,
    title: String,
    heading: String,
    description: String,
    buttonText: String
  }
}
</script>


<template>
  <div class="card-box">
    <div class="card">
      <img :src="imageSrc" alt="Card Image" v-if="imageSrc" />
      <h3>{{ title }}</h3>
      <h1>{{ heading }}</h1>
      <p>{{ description }}</p>
      <button @click="buttonClick">{{ buttonText }}</button>
    </div>
  </div>

</template>

<style lang="scss" scoped>
@use '../scss/main.scss' as *;
.card-box{
  height: 100%;
  display: flex;
  justify-content: center;
  align-items: center;
  .card{
    background-color: white;
    height: 60%;
    width: 70%;
  }

}
</style>