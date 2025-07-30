<template>
    <nav>
        <p>{{ typedText }}</p>
        <ul>
            <li><a href="#">Home</a></li>
            <li><a href="#">Sobre</a></li>
            <li><a href="#">Testemunhos</a></li>
            <li><a href="#">Contatos</a></li>
        </ul>
    </nav>
</template>

<script setup>
import { ref, onMounted } from 'vue'

const texto = "SER DIGITAL";
const typedText = ref('');
const delay = 100;

onMounted(() => {
    const letras = texto.split("");

    letras.forEach((letra, indice) => {
        setTimeout(() => {
            typedText.value += letra;
        }, delay * indice);
    });
});
</script>

<style scoped>
p {
    color: white;
    font-size: 1.8rem;
    font-family: 'Gill Sans', 'Gill Sans MT', Calibri, 'Trebuchet MS', sans-serif;
    font-weight: 600;
}
</style>
