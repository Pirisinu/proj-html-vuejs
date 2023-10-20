<script>
export default {
  name: 'LtlCard',
  props:{
    imageSrc: String,
    imageAlt: String,
    title: String,
    content: String,
    buttonText: String,

  }
}
</script>


<template>
  <div class="card">
    <img :src="imageSrc" alt="img" />
    <h4>{{ title }}</h4>
    <p>{{ content }}</p>
    <button>{{ buttonText }}</button>
  </div>
</template>

<style>

</style>