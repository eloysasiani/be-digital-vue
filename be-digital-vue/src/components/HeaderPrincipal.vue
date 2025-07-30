<template>
    <div class="headerprincipal">
        <section class="principal">
            <div>
                <h1>{{ otherText }}</h1>
                <p>Somos um time <span>{{ porcentagem }}</span> digital construindo produtos <span>{{ porcentagem
                        }}</span> digitais</p>
                <a href="#"><button>Entre em Contato</button></a>
            </div>
        </section>
        <img :src="onlinebusiness2" alt="">
        <div class="redes-sociais">
            <div class="icon"><img :src="emoji1" alt="Ícone 1"></div>
            <div class="icon"><img :src="emoji2" alt="Ícone 2"></div>
            <div class="icon"><img :src="emoji3" alt="Ícone 3"></div>
            <div class="icon"><img :src="emoji4" alt="Ícone 4"></div>
            <div class="icon"><img :src="emoji5" alt="Ícone 5"></div>
        </div>

    </div>
</template>

<script setup>
import onlinebusiness from "@/assets/images/online-business-marketing.png";
import onlinebusiness2 from "@/assets/images/online-business-marketing-2x.png";
import onlinebusiness3 from "@/assets/images/online-business-marketing-4x.png";
import emoji1 from "@/components/icons/zany.svg";
import emoji2 from "@/components/icons/winking.svg";
import emoji3 from "@/components/icons/upside-down.svg";
import emoji4 from "@/components/icons/cat.svg";
import emoji5 from "@/components/icons/emoji.svg";

import { ref, onMounted } from 'vue'

const text = "Produtos, Marcas & Experiências Digitais!";
const otherText = ref('');
const delay = 100;

onMounted(() => {
    const letras = text.split("");

    letras.forEach((letra, indice) => {
        setTimeout(() => {
            otherText.value += letra;
        }, delay * indice);
    });
});

const secondText = "100%";
const porcentagem = ref('');
const otherDelay = 200;

onMounted(() => {
    const letras = secondText.split("");

    letras.forEach((letra, indice) => {
        setTimeout(() => {
            porcentagem.value += letra;
        }, otherDelay * indice);
    });
});
</script>

<style scoped>
div h1 {
    font-size: 6rem;
    line-height: 7rem;
    color: rgb(45, 0, 87);
}

div p {
    font-size: 1.7rem;
}

div {
    gap: 2rem;
    display: flex;
    flex-direction: column;
}

span {
    font-size: 2rem;

}

button,
button a {
    padding: 1.5rem 3rem 1.5rem 3rem;
    border-radius: 10rem;
    font-size: 1.2rem;

}

.headerprincipal {
    position: relative;
    display: grid;
    grid-template-columns: repeat(2, 1fr);
    grid-column-gap: 2rem;
    min-height: 100vh;
    overflow: hidden;
    background-color: rgb(240, 225, 254);
}

.principal {
    display: flex;
    flex-direction: column;
    justify-content: center;
    align-items: center;
    margin: 6rem;
}

.headerprincipal>img {
    align-self: center;
    justify-self: end;
    max-width: 90%;
    height: auto;
}

.redes-sociais {
    position: absolute;
    top: 0;
    left: 0;
    width: 100%;
    height: 100%;
    pointer-events: none;
    overflow: hidden;
    z-index: 10;
}

.icon {
    position: absolute;
    width: 70px;
    height: 70px;
    opacity: 0.8;
    animation-name: cair;
    animation-timing-function: linear;
    animation-iteration-count: infinite;
    filter: drop-shadow(0 0 2px rgba(0, 0, 0, 0.3));
}



@keyframes cair {
    0% {
        transform: translateY(-50px) translateX(100px) rotate(0deg);
        opacity: 1;
    }

    100% {
        transform: translateY(calc(100% + 80px)) translateX(100%) rotate(360deg);
        opacity: 0;
    }
}



.icon:nth-child(1) {
    left: 5vw;
    animation-duration: 7s;
    animation-delay: 0s;
}

.icon:nth-child(2) {
    left: 15vw;
    animation-duration: 6s;
    animation-delay: 0s;
}

.icon:nth-child(3) {
    left: 25vw;
    animation-duration: 8s;
    animation-delay: 0s;
}

.icon:nth-child(4) {
    left: 30vw;
    animation-duration: 7.5s;
    animation-delay: 0s;
}

.icon:nth-child(5) {
    left: 50vw;
    animation-duration: 6.5s;
    animation-delay: 0s;
}



.icon img {
    width: 100%;
    height: 100%;
    object-fit: contain;
}
</style>
