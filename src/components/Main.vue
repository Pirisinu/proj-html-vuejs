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
<TxtCard
  class=""
  :title="'Ciao'"
  :heading="'Ciao4'"
  :description="'Custom Description '"
  :buttonText="'Click Me'"
>
  <template v-slot:left>
    <span class="line"></span>
  </template>
</TxtCard>
<TxtCard
  class=""
  :title="'Ciao'"
  :heading="'Ciao4'"
  :description="'Custom Description'"
  :buttonText="'Click Me'"
>
  <template v-slot:left>
    <span class="line"></span>
  </template>
</TxtCard>
<TxtCard
  class=""
  :title="'Ciao'"
  :heading="'Ciao4'"
  :description="'Custom Description'"
  :buttonText="'Click Me'"
>
  <template v-slot:left>
    <span class="line"></span>
  </template>
</TxtCard>
      
    
</template>

<style lang="scss" scoped>
@use '../scss/main.scss' as *;

</style>