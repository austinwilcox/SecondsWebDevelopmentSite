<template>
  <b-navbar toggleable="lg" variant="primary">
    <b-navbar-brand to="/">Seconds Web Dev</b-navbar-brand>
    <b-navbar-toggle target="nav-collapse"></b-navbar-toggle>
    <b-collapse id="nav-collapse" is-nav>
      <!-- Right aligned nav items -->
      <b-navbar-nav class="ml-auto">
        <b-button variant="primary" to="/ContactMe">Contact Me</b-button>
        <b-button variant="primary" to="/OpenSource">Open Source</b-button>
      </b-navbar-nav>
    </b-collapse>
  </b-navbar>
</template>

<script>
export default {

}
</script>

<style>

</style>