<script setup>
import Sidebar from "./components/Sidebar.vue";
import Header from "./components/Header.vue";
import Footer from "./components/Footer.vue";
import PortfolioSection from "./components/PortfolioSection.vue";
import p01 from './assets/p-01.png';
import p02 from './assets/p-02.png';
import p03 from './assets/p-03.png';
import p04 from './assets/p-04.png';
import p06 from './assets/p-06.png';
import p07 from './assets/p-07.png';
import p08 from './assets/p-08.png';
import p11 from './assets/p-11.png';
import p12 from './assets/p-12.png';
import p13 from './assets/p-13.png';

const DataWebsite = [
  {"technologys":['VanillaJS'] , "gallery":p07, "url":"http://maxx.lionfree.net/gard/"},
  {"technologys":['jQuery'] , "gallery":p01, "url":"http://maxx.lionfree.net/villa/"},
  {"technologys":['VanillaJS'] , "gallery":p03 , "url":"http://maxx.lionfree.net/osicbio"},
  {"technologys":['VanillaJS'] , "gallery":p08, "url":"http://maxx.lionfree.net/wulala"},
  {"technologys":['VanillaJS'] , "gallery":p04, "url":"https://ann-shin.com.tw"},
  {"technologys":['jQuery'] , "gallery":p11, "url":"http://maxx.lionfree.net/jdtver"},
  {"technologys":['jQuery','GASP'] , "gallery":p02, "url":"http://maxx.lionfree.net/landyWen"},
  {"technologys":['jQuery',"GASP"] , "gallery":p06, "url":"http://maxx.lionfree.net/Essential"},
];

const DataApplication = [
  {"technologys":['React'] , "gallery":p12, "url":"https://breewoo.github.io/react-weather-app/"},
  {"technologys":['VanillaJS'] , "gallery":p13, "url":"http://maxx.lionfree.net/vaCalculator/"},
];

</script>

<template>
  <Sidebar />

  <main>
    <Header />

    <PortfolioSection title="Website" :projects="DataWebsite"/>
    <PortfolioSection title="Application" :projects="DataApplication"/>

    <Footer />
  </main>

</template>

<style lang="scss">
main{
  padding: 30px 30px 30px 80px;

  @media screen and (max-width:600px) { 
    padding: 20px 20px 20px 50px;
  }
}

</style>
