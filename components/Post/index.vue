<template>
  <section class="blog-pg single section-padding">
    <div class="container">
      <div class="row justify-content-center">
        <div class="col-lg-11">
          <div class="post">
            <PostHead :postData="postData" />
            <PostContent />
            <PostPagination />
            <PostComments :comments="postData.comments" />
            <PostForm />
          </div>
        </div>
      </div>
    </div>
  </section>
</template>

<script setup>
//= Components
import PostHead from "./Post-Head";
import PostContent from "./Post-Content";
import PostPagination from "./Post-Pagination";
import PostComments from "./Post-Comments";
import PostForm from "./Post-Form";
//= Static Data
import postData from "@/data/blog.json";
</script>
