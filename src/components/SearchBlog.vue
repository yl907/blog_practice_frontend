<script setup>
  import { ref } from 'vue'
  import Blog from './Blog.vue'

  let id = ref("");
  let title = ref("");
  let content = ref("");

  function searchBlogById() {
    // get input id
    const input_id = document.querySelector("#inputID").value;
    // use fetch API to request
    fetch(`http://localhost:8080/blog/${input_id}`)
      .then(response => response.json())
      .then(data => {
        // get attribute
        id.value = data.id;
        title.value = data.title;
        content.value = data.content;
      })
      .catch(error => console.error('Error:', error));
  }
</script>

<template>
  <div class="box">  
    <div>
      <label for="inputID">input id:</label>
      <input type="text" id="inputID" name="id"/> 
      <button @click="searchBlogById" id="searchBlogButton">search blog</button> 
    </div>
    
    <div class="">
      <Blog :id="id" :title="title" :content="content"></Blog>
    </div>
  </div>
</template>


<style scoped>
  .box {
    border: 2px solid rgb(0, 0, 0) ;
    border-radius: 2em;
    margin: 1em;
    padding: 1em;
  }

  button {
    border-radius: 1em;
    margin-left: 1em;
  }

</style>

