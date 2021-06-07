<template>
  <div>
    <b-jumbotron>
      <p class="container lead">Publications</p>
    </b-jumbotron>
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
  head() {
    return {
      title: `${this.posts.length} Publications`,
      meta: [
        {
          hid: "description",
          name: "description",
          content: `Consultez les ${this.posts.length} publications`,
        },
      ],
    };
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
.lead {
  font-size: 30px !important;
  font-weight: bold;
}
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