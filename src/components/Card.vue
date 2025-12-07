<script setup>
import { Icon } from "@iconify/vue";
// Definindo a Props
defineProps(["imagem"]);

function clickFav() {
    const coracao = document.getElementById("coracao");
    if (coracao.style.color == 'white') {
      coracao.style.color = 'red';
    } else {
      coracao.style.color = 'white';
    }
  }
</script>

<template>
    <section class="card">
        <div>
            <button onclick="clickFav()"><Icon id="coracao" icon="pixel:heart-solid" width="24" height="24" /></button>
            <img :src="imagem" alt="Praia de São Conrado" />
        </div>
    </section>
</template>

<style scoped lang="scss">
.card {
    width: 30vw;
    height: 50vh;
    position: relative;

    img {
        border-radius: 10px;
        width: 100%;
        height: 100%;
    }

    button {
        font-size: 24px;
        position: absolute;
        right: 15px;
        top: 10px;
        background-color: transparent;
        border: none;
        cursor: pointer;

        #coracao {
            color: white;
        }
    }
}
</style>
