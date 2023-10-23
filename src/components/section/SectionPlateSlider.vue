<script>

import SliderComp from '../SliderComp.vue';
export default {
  name: 'SectionPlateSlider',
  components:{
    SliderComp
  }
}
</script>

<template>
  <section>
    <SliderComp :sliderData="sliderData"/>
  </section>
</template>

<style lang="scss" scoped>

</style>