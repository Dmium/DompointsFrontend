<template>
  <b-navbar toggleable="md" type="dark" variant="dark">
    <b-navbar-toggle target="nav_collapse"></b-navbar-toggle>
    <b-navbar-brand href="#">Dom Points</b-navbar-brand>
    <b-collapse is-nav id="nav_collapse">
      <b-navbar-nav>
        <router-link to="/" class=nav-link>Home</router-link>
        <router-link to="/about" class=nav-link>About</router-link>
        <router-link to="/test" class=nav-link>Test</router-link>
      </b-navbar-nav>
    </b-collapse>
  </b-navbar>
</template>
