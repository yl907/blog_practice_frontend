<script setup>
  import { ref } from 'vue';

  let input_id = ref('');

  function deleteBlogById() {
    input_id = document.querySelector("#deleteID").value;
    fetch(`http://localhost:8080/blog/deleteBlog/${input_id}`);

    
    return;
  }
</script>

<template>
  <div class="box">
    <h2>Delete Blog</h2>
    <div>
      <label for="deleteID">ID:</label>
      <input type="text" id="deleteID">
      <button id="deleteButton" @click="deleteBlogById">delete blog</button>
    </div>
  </div>
</template>

<style scoped>
  .box {
    border: 2px solid rgb(192, 70, 70) ;
    border-radius: 2em;
    margin: 1em;
    padding: 2em;

    h2 {
      position: relative;
      margin-top: 0px;
    }

  }

  button {
    border-radius: 1em;
    margin-left: 1em;
  }
</style>
