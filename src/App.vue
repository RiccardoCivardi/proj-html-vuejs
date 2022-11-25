<script>

/* Import components: AppHeader, AppMain, AppFooter */
import AppHeader from './components/AppHeader.vue';
import AppMain from './components/AppMain.vue';
import AppFooter from './components/AppFooter.vue';

export default {

  name: 'App',

  components: {

    AppHeader,
    AppMain,
    AppFooter

  }

}

</script>

<template>

  <AppHeader/>

  <button class="btn btn-primary text-white">primary</button>
  <button class="btn btn-outline-primary">secdbhkeb</button>
  
  

  <AppMain/>

  <AppFooter/>

</template>

<style lang="scss">

@use './style/general.scss'

</style>
