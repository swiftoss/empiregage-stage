<template>
  <div>
    <SideNavbar />
    <HeaderSearch />
    <OverviewData />
    <GrafiekTest />
  </div>
</template>

<script>
import SideNavbar from './components/SideNavbar.vue';
import HeaderSearch from './components/HeaderSearch.vue';
import OverviewData from './components/OverviewData.vue';
import GrafiekTest from './components/GrafiekTest.vue';

export default {
  name: 'App',
  components: {
    SideNavbar,
    HeaderSearch,
    OverviewData,
    GrafiekTest
  },
}

</script>

<style>
 body{
  margin: 0;
 }
</style>
