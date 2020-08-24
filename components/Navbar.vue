<template>
  <b-navbar toggleable="lg" type="dark" id="navbar" sticky>
    <b-navbar-brand to="/" style="color: white;">Seconds Web Development</b-navbar-brand>
    <b-navbar-toggle target="nav-collapse"></b-navbar-toggle>
    <b-collapse id="nav-collapse" is-nav>
      <b-navbar-nav class="ml-auto">
        <b-nav-item to="/aboutme">About Me</b-nav-item>
        <b-nav-item to="/blog">Blog</b-nav-item>
        <b-nav-item to="/codeSnippets">Code Snippets</b-nav-item>
        <b-nav-item to="/openSource">Open Source</b-nav-item>
        <b-nav-item to="/resume">Resume</b-nav-item>
        <b-nav-item to="/services">Services</b-nav-item>
      </b-navbar-nav>
    </b-collapse>
  </b-navbar>
</template>

<script>
export default {
}
</script>

<style>
#navbar {
  background-color: #094074;
}
</style>