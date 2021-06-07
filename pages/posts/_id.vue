<template>
  <div class="container">
    <Post :post="post" />
  </div>
</template>

<script>
import axios from "axios";
import Post from "../../components/Post.vue";

export default {
  components: { Post },
  data() {
    return { post: {} };
  },
  head() {
    return {
      title: this.post.title,
    };
  },
  async fetch() {
    console.log(this.$route);
    await axios
      .get(
        "https://jsonplaceholder.typicode.com/posts/" + this.$route.params.id
      )
      .then((response) => {
        this.post = response.data;
      });
  },
};
</script>

<style>
h1 {
  font-size: 35px;
}
</style>