<template>
  <div>
    <HelloWorld />
    <SideNavbar />
  </div>
</template>

<script>
import HelloWorld from './components/HelloWorld.vue';
import SideNavbar from './components/SideNavbar.vue';

export default {
  name: 'App',
  components: {
    HelloWorld,
    SideNavbar
  }
};
</script>

<style>
/* Voeg hier je stijlregels toe */
</style>
