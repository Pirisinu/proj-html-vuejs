<script>
import LtlCard from '../card/LtlCard.vue';
export default {
  name: 'SectionFoodExperience',
  components:{
    LtlCard
  }
}
</script>

<template>
  <section class="container food-experience">
    <div class="top">
      <div class="content">
        <p><strong>HAC TELLUS, FELIS RISUS AT</strong> mattis mattis. Eget euismod semper egot tortor, donec amet, blandit. Tristiquen facilisi faucibus elementum feugiat in nam in feugait. Ipsum odio etiam duis facilisis amet vulputate.</p>
        <h3>food is our common ground, a universal experience.</h3>
        <p>Tristique tempus condimentum diam donec. Condimentum Uillamcorper sit elementum hendrerit mi nulla in consequat, ut. Metus, nullam sclerisque netus viverra dui.</p>
        <img class="signature" src="../../assets/img/signature-200x172.jpg" alt="">
      </div>
      <div class="img-cont">
        <span>california rolls - $22</span>
      </div>
    </div>

    <div class="bottom">
      <LtlCard/>
    </div>
  </section>
</template>

<style lang="scss" scoped>
section.food-experience{
  .top{
    display: flex;
    justify-content: space-between;

    .content{
      width: 40%;
      margin: 40px;
      display: flex;
      flex-direction: column;
      justify-content: space-between;
      
      h3{
        font-size: 2.5rem;
        text-transform: uppercase;
        font-weight: 600;
        letter-spacing: -1px;
      }
      img.signature{
        height: 80px;
        width: 30%;
      }
    }
    .img-cont{
      height: 600px;
      width: 400px;
      background: linear-gradient(rgba(0,0,0,.1) 80% , rgba(0,0,0,.8) 95%), url('/info22x.jpg');
      background-size: cover;
      background-position: center;
      display: flex;
      justify-content: center;
      align-items: end;
      img{
        height: 100%;
        width: 100%;
        object-fit: cover;
      }
      span{
        color: white;
        text-transform: uppercase;
        font-size: .9rem;
        margin-bottom: 10px;
      }
    }
  }
  .bottom{
    margin-top: 80px;
  }
}

</style>