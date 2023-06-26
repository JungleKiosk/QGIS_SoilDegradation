<script>

import { links } from './data/linkVideo.js';

import AppHeader from './components/AppHeader.vue';
import Jumbotron from './components/Jumbotron.vue';
import FeaturesHistory from './components/FeaturesHistory.vue';
import SoilDegradation from './components/SoilDegradation.vue';
import BannerCards from './components/BannerCards.vue';
import MorfClimate from './components/MorfClimate.vue';
import Salinity from './components/Salinity.vue';
import Compaction from './components/Compaction.vue';
import Agronomic from './components/Agronomic.vue';
import RemoteSensing from './components/RemoteSensing.vue';
import AppFooter from './components/AppFooter.vue';

export default {
  data() {
    return {
    };
  },
  components: { AppHeader, Jumbotron, FeaturesHistory, SoilDegradation, BannerCards, MorfClimate, Salinity, Compaction, Agronomic, RemoteSensing, AppFooter },
  computed: {
    linksData() {
      return links;
    }
  }
}

</script>

<template>
  <AppHeader></AppHeader>
  <Jumbotron></Jumbotron>
  <FeaturesHistory></FeaturesHistory>
  <SoilDegradation></SoilDegradation>
  <BannerCards :links="linksData"></BannerCards>
  <MorfClimate></MorfClimate>
  <Salinity></Salinity>
  <Compaction></Compaction>
  <Agronomic></Agronomic>
  <RemoteSensing></RemoteSensing>
  <AppFooter></AppFooter>
</template>

<style></style>
