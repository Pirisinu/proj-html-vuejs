<script>
export default {
  name: 'MenuCard',
  props: {
    menu: Object,
    isSelected: Boolean
  },
  methods: {
    handleCardClick() {
      this.menu.isSelected = !this.menu.isSelected;
      this.$emit('clickCard', this.menu.isSelected);
    }
  }
}
</script>


<template>
  <div 
    class="menu-card"
    @click="handleCardClick"
    :class="{ 'selected': isSelected }"
  >
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
@use '../scss/main.scss' as *;
  .menu-card { 
    background-color: $grey;
    width: 500px;
    height: 700px;
    padding: 60px 50px;
    margin: 40px 0;
    display: inline-block;
    cursor: pointer;
    

    &.selected{
      border: 2px solid black;
      margin: 0px 0px 80px;
      color: white;
    }
    &:nth-child(1),
    &:nth-child(2),
    &:nth-child(3){
      background-size: cover;
      background-position: center;
    }
    &:nth-child(1) {
    background-image: url('../assets/img/mm-1.jpg');
    }
    &:nth-child(2) {
      background-image: linear-gradient(to bottom, rgba(0, 0, 0, 1), rgba(0, 0, 0, 0.5)), url('../assets/img/misc22x.jpg');
    }
    &:nth-child(3) {
    background-image: url('../assets/img/mm-3.jpg');
    }
    &:not(.selected) {
    background-image: none;
  }
}
</style>