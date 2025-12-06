<script setup>
import { ref } from 'vue';
import Card from './Card.vue';

// Ele nos permite buscar dados de APIs externas de forma simples.
import axios from "axios";

// Criamos uma variável reativa que vai guardar a lista de imagens. Começa vazia para depois ser preenchida.
const imagens = ref([]);

// Função assíncrona - que busca as imagens de uma API externa. Pode ser rápida ou demorada, dependendo da conexão.
async function carregarImagens() {
    // variável res é a resposta da requisição feita com o axios
    // await significa que pode esperar a resposta, não sendo instantâneo
    const res = await axios.get("https://picsum.photos/v2/list?page=2&limit=10");

    imagens.value = res.data;

    console.log(res);
}

carregarImagens();
</script>

<template>
    <section class="inspire">
        <h2>Inspire-se</h2>
        <article class="cards">
            <!-- Consumo de API considerando a props que foi criada para cada imagem -->
            <Card v-for="img in imagens" :imagem="img.download_url" />
        </article>
        
    </section>
</template>

<style scoped lang="scss">
.inspire {
    margin: 2rem;
    display: flex;
    flex-direction: column;


}

.cards {
  display: flex;
  flex-wrap: wrap;
  justify-content: space-evenly;
  align-items: center;
  gap: 1rem;
}
</style>