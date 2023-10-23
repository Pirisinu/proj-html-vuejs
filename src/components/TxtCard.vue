<script>
export default {
  name: 'TxtCard',
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
        <slot class="left" name="left"></slot>

      <div class="content">
        <img :src="imageSrc" alt="Card Image" v-if="imageSrc" />
        <h3 class="title">{{ title }}</h3>
        <span class="ltl-price">{{ ltlPrice }}</span>
        <h1 class="heading">{{ heading }}</h1>
        <p class="description">{{ description }}</p>
        <button @click="buttonClick">{{ buttonText }}</button>
      </div>
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
    height: 60%;
    width: 70%;
    display: flex;
    .content{
      width: 100%;
      color: $grey;
      position: relative;
      
      button{
        color: white;
        font-size: 18px;
        background-color: rgba(0, 0, 0, 0.288);
        border: 1px solid gray;
        padding: 7px 27px;
        margin: 80px 0 0;

        &:hover{
          background-color: $grey;
          color: $black;
        }
      }
      .title{
        color: rgb(161, 161, 161);
        font-weight: 300;
      }
      .ltl-price{
        position: absolute ;
        font-size: .9rem;
        right: -20px;
        top: 60px;
      }
      .heading{
        font-size: 50px;
        font-weight: 600;
        color: $white;
        margin: 40px 0;
      }
      .description{
        font-weight: 300;
        font-size: 20px;
        color: rgb(161, 161, 161);
      }
      .title, .heading{
        text-transform: uppercase;
      }
    }
  }

}
</style>