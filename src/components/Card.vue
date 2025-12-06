<script setup>
// NOVO CONTEÚDO: Props
defineProps(["imagem"]);
</script>

<template>
    <section class="card">
        <div>
        <!-- NOVO CONTEÚDO: Props -->
            <button>❤️</button>
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
        right: 10px;
        background-color: transparent;
        border: none;
        cursor: pointer;
    }
}
</style>
