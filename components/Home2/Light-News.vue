<template>
  <section class="blog-grid center bg-gray section-padding">
    <div class="container">
      <div class="section-head text-center">
        <div class="row justify-content-center">
          <div class="col-lg-6 col-md-8 col-sm-10">
            <h6 class="custom-font wow fadeInDown" data-wow-delay=".3s">Latest News</h6>
            <h4 class="playfont wow flipInX" data-wow-delay=".5s">Our Blogs</h4>
          </div>
        </div>
      </div>
      <div class="row">
        <div class="col-md-6" v-for="blog, idx in blogs" :key="idx">
          <div :class="`item wow fadeInUp ${idx !== blogs.length - 1 ? 'md-mb50' : ''}`" data-wow-delay=".3s">
            <div class="post-img">
              <div class="img">
                <img :src="blog.image" alt="">
              </div>
            </div>
            <div class="cont">
              <div class="info">
                <a href="#0">{{ blog.author }}</a>
                <a href="#0">{{ blog.date }}</a>
              </div>
              <h5 class="playfont">
                <a href="#0">{{ blog.title }}</a>
              </h5>
              <a href="/blog-details" class="more">
                <span class="custom-font">Read More</span>
              </a>
            </div>
          </div>
        </div>
      </div>
    </div>
  </section>
</template>

<script setup>
import blogs from '@/data/home2-light-news.json';
</script>
