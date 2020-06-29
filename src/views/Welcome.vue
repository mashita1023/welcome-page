<template>
  <div class="backgrond">
    <Background></Background>
    <Registration></Registration>

  </div>
  
</template>

<style lang="scss">

</style>

<script>
  import Background from '@/components/Background.vue';
  import Registration from '@/components/Registration.vue';

  export default {
    name: 'Welcome',
    components: {
      Background,
      Registration
    }
  }
</script>