<script setup>

</script>

<template>
  <!-- create blog -->
  <div class="box">
    <h2>Create Blog</h2>

    <form action="http://127.0.0.1:8080/blog/createBlog" method="post">
      <ul>
        <li>
          <label for="createdID">ID:</label> <br />
          <input type="text" id="createdID" name="id" >
        </li>
        <li>
          <label for="createdTitle">title:</label> <br />
          <input type="text" id="createdTitle" name="title" >
        </li>
        <li>
          <label for="createdContent">content:</label> <br />
          <textarea id="createdContent" name="content" row="100" column="100"></textarea>
        </li>
      </ul>

      <div>
        <button type="submit">create blog</button>
      </div>
    </form>
  </div>

</template>

<style scoped>
  .box {
    border: 2px solid rgb(103, 179, 255) ;
    border-radius: 2em;
    margin: 1em;
    padding: 2em;

    h2 {
      position: relative;
      margin-top: 0px;
    }

    ul {
      list-style-type: none;
      padding-left: 0px;
    }

    button[type="submit"] {
      position: relative;
      /* 等会有空搞一下居中 */
    }
  }

  #createdContent {
    width: 80vw;
    height: 20vh;  
  }

</style>

