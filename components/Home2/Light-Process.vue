<template>
  <section class="process section-padding bg-img bg-repeat" data-background="/img/dots.png">
    <div class="container">
      <div class="section-head text-center">
        <div class="row justify-content-center">
          <div class="col-lg-6 col-md-8 col-sm-10">
            <h6 class="custom-font wow fadeInDown" data-wow-delay=".3s">How We Do It</h6>
            <h4 class="playfont wow flipInX" data-wow-delay=".5s">Work Process</h4>
          </div>
        </div>
      </div>
      <div class=" row">
        <div :class="`col-lg-3 col-md-6 ${idx !== steps.length - 1 ? 'coulmn' : ''} wow fadeInUp`"
          :data-wow-delay="`${idx / 10 + 0.3}s`" v-for="step, idx in steps" :key="idx">
          <div class="item">
            <div class="bg-img" :style="`background-image:url('${step.image}')`">
              <h3 class="numb custom-font">{{ step.id }}</h3>
            </div>
            <div class="cont">
              <h6 class="mb-10">{{ step.title }}</h6>
              <p>{{ step.text }}</p>
            </div>
          </div>
        </div>
      </div>
    </div>
  </section>
</template>

<script setup>
import steps from "@/data/home2-light-process.json";
</script>
