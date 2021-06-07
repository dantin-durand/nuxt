<template>
  <div class="home">
    <b-jumbotron header="Nuxt" lead="Toutes les publications autour de NUXT">
      <b-button variant="primary" href="#" class="mt-3 cta">Consulter</b-button>
    </b-jumbotron>
  </div>
</template>

<script>
export default {
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
</style>
