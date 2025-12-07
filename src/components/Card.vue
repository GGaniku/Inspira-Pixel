<script setup>
import { Icon } from "@iconify/vue";
// Definindo a Props
defineProps(["imagem"]);

// Função para clicar no coração
const vermelho = 'rgb(255, 0, 0)';
const branco = 'rgb(255, 255, 255)';

function clickFav() {
    const coracao = document.getElementById("coracao");
    if (coracao.style.color == branco) {
      coracao.style.color = vermelho;
    } else {
      coracao.style.color = branco;
    }
  }
</script>

<template>
    <section class="card">
        <div>
            <button @click="clickFav()"><Icon id="coracao" icon="pixel:heart-solid" width="24" height="24" /></button>
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
            color: rgb(255, 255, 255);
        }

        #coracao:hover {
            color: rgb(241, 134, 134);
        }
    }
}
</style>
