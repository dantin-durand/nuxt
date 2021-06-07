<template>
  <div>
    <b-jumbotron lead="Publications"></b-jumbotron>
    <div class="publications">
      <PostItem v-for="(post, index) of posts" :key="index" :post="post" />
    </div>
  </div>
</template>

<script>
import axios from "axios";
import PostItem from "../../components/PostItem.vue";
export default {
  components: { PostItem },
  data() {
    return { posts: [] };
  },
  async fetch() {
    await axios
      .get("https://jsonplaceholder.typicode.com/posts")
      .then((response) => {
        this.posts = response.data;
      });
  },
};
</script>

<style>
.publications {
  display: grid;
  grid-template-columns: 1fr;
  padding: 20px 10%;
  gap: 40px;
}
@media screen and (min-width: 1024px) {
  .publications {
    grid-template-columns: 1fr 1fr 1fr;
  }
}
</style>