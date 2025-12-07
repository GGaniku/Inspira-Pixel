<script setup>
import { Icon } from "@iconify/vue";
</script>

<template>
  <footer>
    <article>
        <div id="contato">
            <h3>Contato</h3>
            <ul>
                <li>contato@inspiralens.com</li>
                <li>Central de ajuda</li>
                <li>Rio de Janeiro - Brasil</li>
            </ul>
        </div>
        <div id="sobre">
            <h3>Sobre</h3>
            <ul>
                <li>Quem somos</li>
                <li>Políticas de Privacidade</li>
                <li>Blog</li>
            </ul>
        </div>
        <div id="cat">
            <h3>Assine nossa Newsletter</h3>
            <input type="email" name="email" id="email" placeholder="Seu e-mail" />
            <button>Inscrever-se</button>
        </div>
    </article>
    <div id="redesSociais">
        <ul>
            <li><a id="facebook"><Icon icon="la:facebook-f" width="24" height="24" /></a></li>
            <li><a id="linkedin"><Icon icon="jam:linkedin" width="24" height="24" /></a></li>
            <li><a id="instagram"><Icon icon="iconoir:instagram" width="24" height="24" /></a></li>
            <li><a id="x"><Icon icon="streamline-logos:x-twitter-logo-solid" width="24" height="24" /></a></li>
        </ul>
    </div>
  </footer>
</template>

<style scoped lang="scss">
footer {
    display: block;
    flex-direction: column;
    justify-content: center;
} 

article {
    display: flex;
    justify-content: space-between;
    align-items: center;
    padding: 2rem;
}

li {
    list-style: none;
}

#redesSociais ul{
    display: flex;
    justify-content: center;
    flex-direction: row;
    gap: 1rem;
    padding: 2rem;
}

</style>
