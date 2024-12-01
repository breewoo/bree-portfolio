<template>
  <section class="portfolioSection">
    <h1 class="title">{{ title }}</h1>

    <ul class="portfolioList">
      <li v-for="(project, index) in projects" :key="index" ref="portfolioListRefs">
        <a :href="project.url" target="_blank"><img :src="project.gallery"></a>
        <span v-for="(tech, index) in project.technologys" :key="index">{{ tech }}</span>
        <h2>{{ project.title }}</h2>
      </li>
    </ul>

  </section>
</template>

<script setup>
import { ref, onMounted, onUnmounted } from 'vue';
import { gsap } from 'gsap';

const props = defineProps({
  title: String,
  projects: Array
});

const portfolioListRefs = ref([]);

onMounted(() => {
  portfolioListRefs.value.forEach((pf, index)=>{
    gsap.from(pf, {
      duration: 1,
      x: 25,
      y: 25,
      opacity: 0,
      delay: index * 0.2,
      ease: 'elastic.out',
      stagger: 0.2,
    })
  })
});

onUnmounted(() => {
  gsap.killTweensOf(portfolioListRefs.value)
})



</script>

<style lang="scss">
.portfolioSection{
  display: flex;
  flex-direction: column;
  justify-content: flex-start;

  .title{
    background: #e5e3d4;
    color: #c16e57;
    padding: 0 10px;
    margin-right: 10px;
    font-size: 40px;

    @media screen and (max-width:600px) { 
      font-size: 26px;
    }
  }
}

.portfolioList{
  list-style: none;
  display: flex;
  flex-direction: row;
  flex-wrap: wrap;
  justify-content: flex-start;
  gap: 10px;
  width: 100%;
  max-width: 1280px;
  margin: 0;
  padding: 0;


  li{
    width: calc(25% - 10px);
    margin-bottom: 20px;

    @media screen and (max-width:860px) { 
      width: calc(33.3% - 10px);
    }

    @media screen and (max-width:600px) { 
      width: calc(50% - 10px);
    }

    @media screen and (max-width:428px) { 
      width: calc(100% - 10px);
    }

    >a{
      display: block;
      width: 100%;
      object-fit: cover;
      cursor: pointer;
      img{
        display: block;
        width: 100%;
      }
    }

    >h2{
      margin: 5px 0;
      font-size: 16px;
      color: #e5e3d4;
    }

    >span{
      margin: 0 5px 0 0;
      padding: 0 3px;
      font-size: 10px;
      color: #e5e3d4;
      display: inline-block;
      border: 1px solid #e5e3d4;
      border-radius: 50px;
    }


  }
}
</style>