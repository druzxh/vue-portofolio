<script setup lang="ts">
import { RouterLink, RouterView } from 'vue-router'
import BaseHome from './components/BaseHome.vue'
</script>

<template>
  <header>
    <div class="wrapper">
      <BaseHome title="Badrudin" />

      <div class="nav-container">
        <nav>
          <RouterLink to="/">About</RouterLink>
          <RouterLink to="/experience">Experience</RouterLink>
          <RouterLink to="/projects">Projects</RouterLink>
          <RouterLink to="/contact">Contact</RouterLink>
          <RouterLink to="/my-journey">My Journey</RouterLink>
        </nav>
      </div>

      <div class="social-icons">
        <a href="https://github.com/druzxh" target="_blank">
          <i class="fa-brands fa-github"></i>
        </a>
        <a href="https://linkedin.com/in/bdrudin" target="_blank">
          <i class="fa-brands fa-linkedin"></i>
        </a>
        <a href="https://instagram.com/bd.ruu" target="_blank">
          <i class="fa-brands fa-instagram"></i>
        </a>
        <a href="mailto:badrudin.on@gmail.com">
          <i class="fa-regular fa-envelope"></i>
        </a>
      </div>
    </div>
  </header>

  <RouterView />
</template>

<style scoped>
header {
  line-height: 1.5;
  max-height: 100vh;
}

.logo {
  display: block;
  margin: 0 auto 2rem;
}

nav {
  width: 100%;
  font-size: 12px;
  text-align: center;
  margin-top: 2rem;
}

nav a.router-link-exact-active {
  color: var(--color-green-light);
}

nav a.router-link-exact-active:hover {
  background-color: transparent;
}

nav a {
  display: inline-block;
  padding: 0 1rem;
  border-left: 1px solid var(--color-border);
}

nav a:first-of-type {
  border: 0;
}

.social-icons {
  font-size: 1.5rem;
  display: flex;
}

.social-icons a {
  margin-bottom: 1rem;
  margin-right: 15px;

}

.social-icons a:hover {
  color: #fefefe;
  background-color: hsla(160, 100%, 37%, 0.2);
  padding: 0 7px;
  border-radius: 5px;
  transition: background-color 0.3s ease;
}

@media (min-width: 1024px) {
  header {
    display: flex;
    place-items: center;
    padding-right: calc(var(--section-gap) / 2);
  }

  .logo {
    margin: 0 2rem 0 0;
  }

  header .wrapper {
    display: flex;
    place-items: flex-start;
    flex-wrap: wrap;
  }

  nav {
    text-align: left;
    margin-left: -1rem;
    font-size: 1rem;

    padding: 1rem 0;
    margin-top: 1rem;
  }
}


@media (max-width: 768px) {
  .social-icons {
    justify-content: center;
    font-size: 1rem;
  }

  .social-icons a {
    margin-bottom: 5px;
    margin-top: 5px;
    margin-right: 10px;
  }
}
</style>
