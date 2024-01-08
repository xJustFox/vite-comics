<script>
  import AppHeader from './components/AppHeader.vue';
  import AppMain from './components/AppMain.vue';
  import AppBlueBar from './components/AppBlueBar.vue';

  export default{
    components: {
      AppHeader,
      AppMain,
      AppBlueBar
    }
  }
</script>

<template>

  <AppHeader />
  <AppMain />
  <AppBlueBar />

</template>

<style lang="scss">
  @use './styles/generals.scss' as *;
  @use './styles/partials/_variables.scss' as *;


</style>
