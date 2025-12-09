<script setup>
import { Icon } from "@iconify/vue";
import { ref } from 'vue';
// Definindo a Props
defineProps(["imagem"]);

// Função para clicar no coração
const vermelho = 'rgb(255, 0, 0)';
const branco = 'rgb(255, 255, 255)';

const favoritado = ref(false);

function trocarCor() {
    favoritado.value = !favoritado.value;
};
</script>

<template>
    <div class="card">
        <button class="iconePadrao" :class="{ clicou: favoritado }" @click="trocarCor()">
            <Icon id="coracao" icon="pixel:heart-solid" width="24" height="24" />
        </button>
        <img :src="imagem" alt="Imagem da API" />
    </div>
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

    .iconePadrao {
        color: #fffbfb;
        cursor: pointer;
        :deep(svg) {
            color: #fffbfb;
            transition: color 0.3s ease;
            .iconePadrao:hover & {
                color: #ff5270;
            }
        }
    }

    .clicou :deep(svg) {
        color: #ff5270;
    }
}
</style>
