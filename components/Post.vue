<template>
  <div>
    <h1 class="mt-5">{{ post.title }}</h1>
    <p class="mt-5">{{ post.body }}</p>
  </div>
</template>

<script>
export default {
  name: "Post",
  props: ["post"],
};
</script>

<style>
</style>