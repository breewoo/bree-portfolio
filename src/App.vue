<script setup>
import Sidebar from "./components/Sidebar.vue";
import Header from "./components/Header.vue";
import Footer from "./components/Footer.vue";
import PortfolioSection from "./components/PortfolioSection.vue";

const DataWebsite = [
  {"technologys":['VanillaJS'] , "gallery":"./src/assets/p-07.png", "url":"http://maxx.lionfree.net/gard/"},
  {"technologys":['jQuery'] , "gallery":"./src/assets/p-01.png", "url":"http://maxx.lionfree.net/villa/"},
  {"technologys":['VanillaJS'] , "gallery":"./src/assets/p-03.png", "url":"http://maxx.lionfree.net/osicbio"},
  {"technologys":['VanillaJS'] , "gallery":"./src/assets/p-08.png", "url":"http://maxx.lionfree.net/wulala"},
  {"technologys":['VanillaJS'] , "gallery":"./src/assets/p-04.png", "url":"https://ann-shin.com.tw"},
  {"technologys":['jQuery'] , "gallery":"./src/assets/p-11.png", "url":"http://maxx.lionfree.net/jdtver"},
  {"technologys":['jQuery','GASP'] , "gallery":"./src/assets/p-02.png", "url":"http://maxx.lionfree.net/landyWen"},
  {"technologys":['jQuery',"GASP"] , "gallery":"./src/assets/p-06.png", "url":"http://maxx.lionfree.net/Essential"},
];

const DataApplication = [
  {"technologys":['React'] , "gallery":"./src/assets/p-12.png", "url":"https://breewoo.github.io/react-weather-app/"},
  {"technologys":['VanillaJS'] , "gallery":"./src/assets/p-13.png", "url":"http://maxx.lionfree.net/vaCalculator/"},
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
