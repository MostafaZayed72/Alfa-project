<template>
  <section class="projdtal">
    <div class="justified-gallery row">
      <a :href="image" v-for="image, idx in projectDetailsData.details1" :key="idx"
        class="col-xl-4 col-lg-6 col-12 mb-20">
        <img alt="" :src="image" />
      </a>
    </div>
  </section>
</template>

<script setup>
import projectDetailsData from "@/data/project-details.json";
</script>
