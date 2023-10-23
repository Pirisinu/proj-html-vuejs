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
      <button>{{ buttonText }}</button>
    </div>
  </div>

</template>

<style lang="scss" scoped>

  .card-box{
    color: white;
    display: flex;
    justify-content: center;
    align-items: center;
    .card{
      height: 70%;
      width: 60%;

      display: flex;
      flex-direction: column;
      .name,
      .heading,
      .star-container,
      .line,
      .description{
        margin-bottom: 20px;
      }
      .name{
        color: #e8e8e8;
        text-transform: uppercase;
        font-size: .8;
      }
      .heading{
        text-transform: uppercase;
      }
      button{
        background-color: rgba(255, 255, 255, 0);
        border: 1px solid white;
        width: 50%;
        padding: 10px;
        color: white;
        text-transform: uppercase;
        &:hover{
          background-color: rgba(255, 255, 255, 0.1);
        }
      }
    }
  }
</style>