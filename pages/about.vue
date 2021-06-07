<template>
  <div class="container">
    <h1 class="mt-5">A propos</h1>
    <p class="mt-5">
      Lorem ipsum dolor sit amet consectetur adipisicing elit. Exercitationem
      magnam aut quae, voluptatem quisquam animi unde laboriosam ex ab dicta
      dolor cum reprehenderit, accusantium eveniet quod repudiandae voluptatum
      recusandae necessitatibus? Aspernatur rerum, accusamus quos laudantium ad
      hic distinctio suscipit quas, explicabo laboriosam, exercitationem minima
      facilis aliquam commodi provident facere rem doloremque libero quod!
      Perspiciatis delectus voluptatum saepe nemo voluptas ut, nam veniam fugit.
      Totam repudiandae maiores amet numquam distinctio atque voluptate ea velit
      modi, quia dolor deleniti accusamus, officiis qui nesciunt praesentium
      explicabo omnis fuga tempore nisi molestiae ipsum aliquam veritatis quae?
      Quia ex corporis quasi veritatis consequatur, in id!
    </p>
  </div>
</template>

<script>
export default {
  head() {
    return {
      title: "A props de NUXT",
      meta: [
        {
          hid: "description",
          name: "description",
          content: "A propos de NUXT Publications",
        },
      ],
    };
  },
};
</script>

<style scoped>
.cta {
  background: var(--main-gradient) !important;
  border: 1px solid #ffffff78 !important;
  border-radius: 5px;
}
p {
  line-height: 20px;
}
</style>
