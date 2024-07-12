<script setup>
  const props = defineProps(['id', 'title', 'content']);

</script>

<template>
  <p class="id">id: {{ props.id }}</p>
  <p class="title">title: {{ props.title }}</p>
  <p class="content">content: {{ props.content }}</p>

</template>

<style scoped>
  .id {
    border: 1px solid black;
    padding: 1em;
  }

  .title {
    border: 1px solid black;
    padding: 1em;

  }

  .content {
    border: 1px solid black;
    padding: 1em;

  }

</style>
