<template>
  <section class="portfolio full-bg">
    <div class="container-fluid">
      <div class="row">
        <div :class="`col-lg-3 col-md-6 cluom ${idx === 0 ? 'current' : ''}`" :data-tab="`tab-${work.id}`"
          v-for="work, idx in works" :key="idx">
          <div class="info">
            <h6 class="custom-font">{{ work.type }}</h6>
            <h5>{{ work.title }}</h5>
          </div>
          <div class="more">
            <a href="#0">View Project <i class="fas fa-chevron-right"></i></a>
          </div>
        </div>
      </div>
    </div>
    <div class="glry-img">
      <div v-for="work, idx in works" :key="idx" :id="`tab-${work.id}`"
        :class="`bg-img tab-img ${idx === 0 ? 'current' : ''}`" data-overlay-dark="2"
        :style="`background-image:url('${work.image}')`" />
    </div>
  </section>
</template>

<script setup>
//= Scripts
import worksCardEffect from "@/common/worksCardEffect";
//= Static Data
import works from "@/data/home3-works.json";

onMounted(() => {
  worksCardEffect();
});
</script>
