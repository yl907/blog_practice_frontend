<script setup>
import { ref } from 'vue';
import Blog from './components/Blog.vue';
import CreateBlog  from './components/CreateBlog.vue';
import DeleteBlog  from './components/DeleteBlog.vue';
import SearchBlog from './components/SearchBlog.vue';
import UpdateBlog from './components/UpdateBlog.vue';

</script>

<template>
  <header>

  </header>

  <main>
    <!-- search blog -->
    <SearchBlog></SearchBlog>
    
    <!-- create blog -->
    <CreateBlog></CreateBlog>

    <!-- delete blog -->
    <DeleteBlog></DeleteBlog>

    <!-- update existing blog -->
    <UpdateBlog></UpdateBlog>
    
  </main>
</template>

<style scoped>
  #searchBlogButton {
    margin-left: 1em;
  }

</style>
