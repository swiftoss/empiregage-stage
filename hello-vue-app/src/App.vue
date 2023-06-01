<template>
  <div>
    <SideNavbar />
    <HeaderSearch />
    <OverviewTitel />
    <div class="dashboard">
    <div class="overview">
      <OverviewData />
    </div>
    <div class="graph">
      <GrafiekTest />
    </div>
  </div>
  </div>
</template>

<script>
import SideNavbar from './components/SideNavbar.vue';
import HeaderSearch from './components/HeaderSearch.vue';
import OverviewTitel from './components/OverviewTitel.vue';
import OverviewData from './components/OverviewData.vue';
import GrafiekTest from './components/GrafiekTest.vue';

export default {
  name: 'App',
  components: {
    SideNavbar,
    HeaderSearch,
    OverviewTitel,
    OverviewData,
    GrafiekTest
  },
}

</script>

<style>
 body{
  margin: 0;
 }

 .dashboard {
  display: grid;
  grid-template-columns: 1fr 1fr; /* Twee kolommen met gelijke breedte */
  grid-gap: 20px; /* Ruimte tussen de kolommen */
}

.overview {
  grid-column: 1; /* Plaats 'Overviewdata' in de eerste kolom */
}

.graph {
  grid-column: 2; /* Plaats 'GrafiekTest' in de tweede kolom */
}
</style>
