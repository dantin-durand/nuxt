<template>
  <nuxt-link :to="'/posts/' + post.id">
    <b-card
      img-src="https://via.placeholder.com/400x300"
      img-alt="Image"
      img-top
      tag="article"
      class="mb-2"
    >
      <b-card-text>
        {{ post.title }}
      </b-card-text>
    </b-card>
  </nuxt-link>
</template>

<script>
export default {
  name: "PostItem",
  props: ["post"],
};
</script>

<style scoped>
.card {
  border: 0px !important;
  box-shadow: 0px 0px 20px rgb(0 0 0 / 17%);
  height: 100%;
  border-radius: 10px !important;
  overflow: hidden;
}
.card p {
  color: #b721ff;
}
</style>