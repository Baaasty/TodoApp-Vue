<script setup>
import { RouterLink } from "vue-router";
</script>

<template>
  <header>
    <nav class="container">
      <div class="branding">
        <img src="../assets/Todo_Logo.png" alt="vue-todos logo" />
        <h1>Todo App</h1>
      </div>
      <ul class="nav-routes">
        <RouterLink :to="{ name: 'todos' }">Todos</RouterLink>
        <RouterLink :to="{ name: 'about' }">About</RouterLink>
      </ul>
    </nav>
  </header>
</template>

<style lang="scss" scoped>
header {
  background-color: #f1f1f1;

  nav {
    display: flex;
    align-items: center;
    padding: 25px 16px;
    max-width: 1100px;
    margin: 0 auto;

    .branding {
      display: flex;
      align-items: center;
      gap: 8px;

      img {
        max-width: 50px;
      }

      h1 {
        font-size: 24px;
      }
    }

    .nav-routes {
      display: flex;
      flex: 1;
      justify-content: flex-end;
      gap: 12px;
      list-style: none;

      a {
        text-decoration: none;
        color: inherit;
      }
    }
  }
}
</style>