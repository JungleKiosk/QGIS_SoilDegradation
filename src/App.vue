<script>

import AppHeader from './components/AppHeader.vue';
import Jumbotron from './components/Jumbotron.vue';
import FeaturesHistory from './components/FeaturesHistory.vue';
import SoilDegradation from './components/SoilDegradation.vue';

export default {
  data() {
    return {
    };
  },
  components: { AppHeader, Jumbotron, FeaturesHistory, SoilDegradation },
}

</script>

<template>
  <AppHeader></AppHeader>
  <Jumbotron></Jumbotron>
  <FeaturesHistory></FeaturesHistory>
  <SoilDegradation></SoilDegradation>
</template>

<style></style>
