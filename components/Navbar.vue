<template>
  <div>
    <b-navbar toggleable="lg" type="dark">
      <b-navbar-brand href="#">Nuxt Publications</b-navbar-brand>

      <b-navbar-toggle target="nav-collapse"></b-navbar-toggle>

      <b-collapse id="nav-collapse" is-nav>
        <b-navbar-nav class="ml-auto">
          <nuxt-link to="/" class="nav-link">Accueil</nuxt-link>
          <nuxt-link to="/about" class="nav-link">A propos</nuxt-link>
          <nuxt-link to="/posts" class="nav-link">Publications</nuxt-link>
        </b-navbar-nav>
      </b-collapse>
    </b-navbar>
  </div>
</template>

<script>
export default {
  name: "Navbar",
};
</script>

<style>
.navbar {
  background-image: var(--main-gradient) !important;
}
</style>