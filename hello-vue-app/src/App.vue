<template>
  <div>
    <SideNavbar />
    <HeaderSearch />
  </div>
</template>

<script>
import SideNavbar from './components/SideNavbar.vue';
import HeaderSearch from './components/HeaderSearch.vue';

export default {
  name: 'App',
  components: {
    SideNavbar,
    HeaderSearch
  }
};
</script>

<style>
 body{
  margin: 0;
 }
</style>
