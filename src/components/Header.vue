<script setup>
import { Icon } from "@iconify/vue";

// Menu sanduíche para Mobile
function clickNav() {
  const menu = document.getElementById("menu");
  if (menu.style.display == 'block') {
    menu.style.display = 'none';
  } else {
    menu.style.display = 'block';
  }
}
</script>

<template>
  <header>
    <img src="../assets/logo.svg" alt="Logo do Inspira Pixel" />
    <a id="burguer" @click="clickNav()"><Icon icon="ci:menu-alt-01" width="24" height="24" /></a>
    <nav id="menu">
      <ul>
        <li><a href=""><Icon icon="iconoir:search" width="24" height="24" /></a></li>
        <li><a href="">Início</a></li>
        <li><a href="">Galeria</a></li>
        <li><a href="">Favoritos</a></li>
        <li><a href=""><Icon icon="lets-icons:user-light" width="24" height="24" /></a></li>
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

  a {
    cursor: pointer;
  }

  ul {
    display: flex;
    flex-direction: column;
    list-style: none;
    justify-content: space-between;
    align-items: center;
    gap: 1.5rem;

    li {
      display: flex;
      flex-wrap: wrap;
    }

    a {
      display: flex;
      align-items: center;
      text-decoration: none;
      color: black;
    }

    a:hover {
      color: gray;
    }
  }
}
</style>
