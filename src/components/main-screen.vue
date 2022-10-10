<template>
  <div class="main">
    <div class="main-screen">
      <div class="navbar">
        <CommonFrame />
      </div>
    </div>
    <div class="img">
      <ProfileImg />
    </div>
    <div class="card">
      <DigitalVue />
    </div>
    <div class="benefits">
      <BenefitsBlock />
    </div>
    <div class="basement">
      <BasementFrame />
    </div>
  </div>
</template>

<script>
import CommonFrame from './common-frame.vue';
import DigitalVue from './digital-vue.vue';
import ProfileImg from './profile-img.vue';
import BenefitsBlock from './benefits-block.vue';
import BasementFrame from './basement-frame.vue';
export default {
  components: {
    CommonFrame,
    ProfileImg,
    DigitalVue,
    BenefitsBlock,
    BasementFrame,
  },
}
</script>

<style scoped lang="scss">
.main {
  .main-screen {
    display: flex;
    margin: 0 12.5%;
  }
  .navbar {
    display: flex;
    width: 100%;
    flex-direction: column;
  }
  .img {
    width: 100%;
    height: 716px;
    display: flex;
    background-image: linear-gradient(90deg, rgba(0, 0, 0, 0.25) 0%, rgba(0, 0, 0, 0.025) 62.79%), url("/public/img/main-img.png");
    background-size: cover;
    background-position-y: 90%;
    backdrop-filter: blur(1px);
  }
  .card {
    width: 75%;
    flex-wrap: wrap;
    margin-top: 120px;
  }
  .benefits {
    width: 75%;
    flex-wrap: wrap;
    margin: 121px 12.5% 120px;
  }
  .basement {
    width: 100%;
  }
}
</style>