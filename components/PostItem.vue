<template>
  <nuxt-link :to="'/posts/' + post.id">
    <b-card
      img-src="https://picsum.photos/600/300/"
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

<style>
</style>