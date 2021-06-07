<template>
  <div class="container">
    <div v-if="error.statusCode === 404">
      <h1>404</h1>
      <p>Page introuvable :(</p>
    </div>
    <div v-else><h1>Une erreur est survenue</h1></div>
    <nuxt-link to="/" class="btn mt-3 btn-dark">Page d'accueil</nuxt-link>
  </div>
</template>

<script>
export default {
  props: ["error"],
  layout: "error", // nous pouvons definir un layout personnalisé pour la page erreur
};
</script>

<style scoped>
.container {
  display: flex;
  justify-content: center;
  align-items: center;
  height: 50vh;
  flex-direction: column;
  gap: 30px;
}
h1 {
  font-size: 100px;
  background: -webkit-linear-gradient(-20deg, #b721ff 0%, #21d4fd 100%);
  -webkit-background-clip: text;
  -webkit-text-fill-color: transparent;
  font-weight: bold;
  text-align: center;
}

p {
  text-align: center;
  font-size: 30px;
}
</style>