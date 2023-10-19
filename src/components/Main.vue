<script>
import TxtCard from './TxtCard.vue';
export default {
  name: 'Main',
  components:{
    TxtCard
  }
}
</script>


<template>
  <TxtCard imageSrc="" :buttonText="ButtonText">
        <template v-slot:title>
          <h3>Ciao</h3>
        </template>
        <template v-slot:heading>
          <h1>Ciao2</h1>
        </template>
        <template v-slot:description>
          <p>Custom Description</p>
        </template>
      </TxtCard>
      <TxtCard imageSrc="" :buttonText="ButtonText">
        <template v-slot:title>
          <h3>Ciao</h3>
        </template>
        <template v-slot:heading>
          <h1>Ciao2</h1>
        </template>
        <template v-slot:description>
          <p>Custom Description</p>
        </template>
      </TxtCard>
      <TxtCard imageSrc="" :buttonText="ButtonText">
        <template v-slot:title>
          <h3>Ciao</h3>
        </template>
        <template v-slot:heading>
          <h1>Ciao2</h1>
        </template>
        <template v-slot:description>
          <p>Custom Description</p>
        </template>
      </TxtCard>
</template>

<style lang="scss" scoped>
@use '../scss/main.scss' as *;
h1{
  color: red;
}
</style>