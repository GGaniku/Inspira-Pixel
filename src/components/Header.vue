<script setup>
import { Icon } from "@iconify/vue";
</script>

<template>
  <header>
    <img src="../assets/logo.svg" alt="" />

    <nav>
      <ul>
        <li><a href="">Lupa</a></li>
          <Icon icon="material-symbols:search-rounded" width="24" height="24" />
        <li><a href="">Início</a></li>
          <Icon icon="material-symbols:home-outline-rounded" width="24" height="24" />
        <li><a href="">Galeria</a></li>
          <Icon icon="material-symbols:home-storage-outline-sharp" width="24" height="24" />
        <li><a href="">Favoritos</a></li>
          <Icon icon="material-symbols:favorite-outline" width="24" height="24" />
        <li><a href="">Usuário</a></li>
          <Icon icon="material-symbols:person" width="24" height="24" />
      </ul>
    </nav>
  </header>
</template>

<style scoped lang="scss">
header {
  display: flex;
  justify-content: space-between;
  align-items: center;
  margin: 2rem;

  ul {
    display: flex;
    list-style: none;
    justify-content: space-evenly;
    gap: 1rem;

    a {
      text-decoration: none;
      color: black;
    }
  }
}

</style>
