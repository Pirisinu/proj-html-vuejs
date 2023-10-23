<script>
export default {
  name: 'Footer'
}
</script>


<template>
  <footer>
    <div class="img-back">
      <div class="footer-container">
        <div class="footer-logo">
          <img src="../assets/img/logo-restaurant-2x-400x77.png" alt="">
        </div>
        <p>Quam eu proin sit massa condimentum. Volutpat non pulvinar aliquet nunc. Quam eu proin sit massa condimentum.</p>
        <div class="icon-container">
          <div class="cercle-box">
            <i class="fa-brands fa-facebook-f"></i>
          </div>
          <div class="cercle-box">
            <i class="fa-brands fa-twitter"></i>
          </div>
          <div class="cercle-box">
            <i class="fa-brands fa-youtube"></i>
          </div>
          <div class="cercle-box">
            <i class="fa-brands fa-instagram"></i>
          </div>
          <div class="cercle-box">
            <i class="fa-brands fa-linkedin-in"></i>
          </div>
        </div>
      </div>
    </div>
    <div class="bottom">
      <p>Copyright 2012 - 2019 Avada</p>
      <p>All Rights Reserved</p>
      <p>Powered by <strong>WorldPress</strong></p>
      <p>Copyright 2012</p>
    </div>
  </footer>
  
</template>

<style lang="scss" scoped>


footer{
  .img-back{
    height: 660px;
    width: 100%;
    background-image: url('../assets/img/footer2x.jpg');
    background-position: center;
    background-size: cover;
    display: flex;
    justify-content: center;
    align-items: center;
    color: white;

    .footer-container{
      height: 50%;
      width: 30%;
      display: flex;
      flex-direction: column;
      justify-content: space-between;
      text-align: center;

      .footer-logo{
        height: 80px;
        img{
          object-fit: contain;
        }
      }
      p{
        font-size: 18px;
  
      }
      .icon-container{
        display: flex;
        justify-content: center;

        .cercle-box{
          border-radius: 50%;
          height: 50px;
          width: 50px;
          margin: 10px;
          background-color: white;
          display: flex;
          justify-content: center;
          color: black;
          i{
            font-size: 1.5rem;
            line-height: 58px;
          }
        }
      }
    }
  }
  .bottom{
    height: 75px;
    background-color: black;
    color: white;
    display: flex;
    justify-content: center;
    align-items: center;
  
    p{
      margin: 0 10px;
    }
  }

}
</style>