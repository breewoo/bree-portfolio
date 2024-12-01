<script setup>
import { ref, onMounted } from 'vue';
import { gsap } from 'gsap';

const avatarImgRef = ref(null);
const avatarNameRef = ref(null);
const titleRef = ref(null);

onMounted(() => {
  gsap.from(avatarImgRef.value, {
    opacity: 0,
    scale: 0.3,
    ease: 'ease-in-out-trans',
    duration: 1
  })
  gsap.from(avatarNameRef.value, {
    opacity: 0,
    x: 50,
    letterSpacing: '100px',
    ease: 'power2.inOut',
    duration: 1.5,
    delay: 0.5
  })
  gsap.from(titleRef.value, {
    opacity: 0,
    x: -150,
    letterSpacing: '50px',
    ease: 'power2.inOut',
    duration: 1.5,
    delay: 1
  })

});

</script>

<template>
  <header>
    <div class="avatar">
      <img src="../assets/avatar.png" ref="avatarImgRef">
      <span ref="avatarNameRef">BREE</span>
    </div>
    <div class="title" ref="titleRef">PORTFOLIO<span>''</span></div>
  </header>
</template>

<style lang="scss">
.avatar {
  display: flex;
  flex-direction: row;
  justify-content: start;
  align-items: center;
  

  >img{
    width: 100px;
    border-radius: 50%;
    margin-right: 30px;

    @media screen and (max-width:860px) { 
      width: 80px;
      margin-right: 15px;
    }

    @media screen and (max-width:600px) { 
      width: 55px;
    }

    @media screen and (max-width:428px) { 
      width: 46px;
    }
  }

  >span{
    font-size: 100px;
    color: #E5E3D4;
    font-weight: bold;

    @media screen and (max-width:860px) { 
      font-size: 80px;
    }

    @media screen and (max-width:600px) { 
      font-size: 55px;
    }

    @media screen and (max-width:428px) { 
      font-size: 46px;
    }
  }
}

.title{
  font-size: 100px;
  color: #3d2b27;
  font-weight: bold;

  @media screen and (max-width:860px) { 
    font-size: 80px;
  }

  @media screen and (max-width:600px) { 
    font-size: 55px;
  }

  @media screen and (max-width:428px) { 
      font-size: 46px;
    }
  span{
    color: #E5E3D4;
  }
}

</style>