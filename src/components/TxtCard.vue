<script>
export default {
  name: 'TxtCard',
  props:{
    title: String,
    heading: String,
    description: String
  }
}
</script>


<template>
<div class="card-box">
  <div class="card">
    <img :src="imageSrc" alt="Card Image" v-if="imageSrc" />
    <slot name="title">Default Title</slot>
    <slot name="heading">Default Heading</slot>
    <slot name="description">Default Description</slot>
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