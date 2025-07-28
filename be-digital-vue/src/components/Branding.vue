<template>
 <section class="branding">
        <p class="brand">Algumas empresas que confiam em nossos serviços:</p>
        <div class="container">
            <img :src="spotify" alt="">
            <img src="./assets/images/slack.svg" alt="">
            <img src="./assets/images/dropbox.svg" alt="">
            <img src="./assets/images/zoom.svg" alt="">
        </div>
    </section>
</template>
<script setup>
import spotify from "@/assets/images/spotify.svg"
</script>
<style scoped>
</style>