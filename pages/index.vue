<template>
  <div class="home">
    <b-jumbotron header="Nuxt" lead="Toutes les publications autour de NUXT">
      <nuxt-link to="/posts" class="btn mt-3 cta btn-primary"
        >Consulter</nuxt-link
      >
    </b-jumbotron>
    <h2>Dernières publications</h2>
    <div class="publications">
      <PostItem v-for="(post, index) of posts" :key="index" :post="post" />
    </div>
  </div>
</template>

<script>
import axios from "axios";
import PostItem from "../components/PostItem.vue";

export default {
  components: { PostItem },
  data() {
    return { posts: [] };
  },
  head() {
    return {
      title: "Bienvenue sur NUXT Publication",
      meta: [
        {
          hid: "description",
          name: "description",
          content: "Bienvenue sur NUXT Publication",
        },
      ],
    };
  },
  async fetch() {
    await axios
      .get("https://jsonplaceholder.typicode.com/posts")
      .then((response) => {
        let data = [];
        for (const key in response.data) {
          if (key < 3) data.push(response.data[key]);
        }
        this.posts = data;
      });
  },
};
</script>

<style scoped>
.home {
  text-align: center;
}
.home .jumbotron {
  height: 50vh;
  display: flex;
  flex-direction: column;
  justify-content: center;
  align-items: center;
  gap: 20px;
}
h2 {
  font-size: 20px;
  margin: 15px 0;
}
</style>
