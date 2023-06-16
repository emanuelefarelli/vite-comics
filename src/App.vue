<script>
  import AppHeader from './components/AppHeader.vue';
  import AppMain from './components/AppMain.vue';
  import AppNav from './components/AppNav.vue';
  import AppFooter from './components/AppFooter.vue';
  import SignIn from './components/SignIn.vue';

  export default{
    name: 'App',
    components:{
      AppHeader,
      AppMain,
      AppNav,
      AppFooter,
      SignIn,
    }
  }
</script>

<template>
  <AppHeader/>
  <AppMain/>
  <AppNav/>
  <AppFooter/>
  <SignIn/>
</template>

<style lang="scss">
  @import './styles/general.scss';
</style>
