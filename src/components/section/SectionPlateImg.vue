<script>
export default {
  name: 'SectionPlateImg'
}
</script>

<template>
  <section class="plate-example">
    <p>KUNG PAO CHICKEN - $32</p>
  </section>
</template>

<style lang="scss" scoped>
/* PLATE-EXAMPLE */
section.plate-example{
  height: 700px;
  background-image: url('/page52x.jpg');
  background-size: cover;
  background-position: center;
  display: flex;
  justify-content: center;
  align-items: end;
  p{
    color: white;
    padding: 15px;
    border-radius: 20px;
    background-color: rgba(0, 0, 0, .5);
  }
}
</style>