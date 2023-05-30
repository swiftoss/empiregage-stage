<template>
  <div>
    <SideNavbar />
    <HeaderSearch />
    <OverviewData />
  </div>
</template>

<script>
import SideNavbar from './components/SideNavbar.vue';
import HeaderSearch from './components/HeaderSearch.vue';
import OverviewData from './components/OverviewData.vue';

export default {
  name: 'App',
  components: {
    SideNavbar,
    HeaderSearch,
    OverviewData
  }
};
</script>

<style>
 body{
  margin: 0;
 }
</style>
