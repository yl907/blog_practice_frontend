<script setup>

</script>

<template>
  <!-- update blog -->
  <div class="box">
    <h2>Update Blog</h2>

    <form action="http://127.0.0.1:8080/blog/updateBlog" method="post">
        <ul>
        <li>
          <label for="ID">ID:</label> <br />
          <input type="text" id="ID" name="id" >
        </li>
        <li>
          <label for="updatedTitle">title:</label> <br />
          <input type="text" id="updatedTitle" name="newTitle" >
        </li>
        <li>
          <label for="updatedContent">content:</label> <br />
          <textarea id="updatedContent" name="newContent" row="100" column="100"></textarea>
        </li>
      </ul>

      <div class="submitButtonContainer">
        <button type="submit">update blog</button>
      </div>
    </form>
  </div>

</template>

<style scoped>
  .box {
    border: 2px solid rgb(87, 255, 163) ;
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

    .submitButtonContainer {
      display: flex;
      /* 居中submit button */
      align-items: center;
      justify-content: center;

      button[type="submit"] {
        border-radius: 1em;
      }
    }
  }

  #updatedContent {
    width: 80vw;
    height: 20vh;  
  }

</style>

