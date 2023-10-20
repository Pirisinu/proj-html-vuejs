<script>
export default {
  name: 'MenuCard',
  props:{
    menu: Object
  }
}
</script>


<template>
  <div class="menu-card">
    <h2 class="name-menu">{{ menu.nameMenu }}</h2>
    <div class="plate">
      <div class="top" v-for="plate in menu.plate" :key="plate.namePlate">
        <h3 class="name-plate">{{ plate.namePlate }}</h3>
        <span class="price">{{ plate.price }}</span>
        <p class="description">{{ plate.description }}</p>
      </div>
    </div>
  </div>
</template>

<style lang="scss" scoped>

</style>