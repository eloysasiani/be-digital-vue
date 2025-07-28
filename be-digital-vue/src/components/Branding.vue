<template>
    <section class="branding">
        <p class="brand">Algumas empresas que confiam em nossos serviços:</p>
        <div class="container">
            <img :src="spotify" alt="">
            <img :src="slack" alt="">
            <img :src="dropbox" alt="">
            <img :src="zoom" alt="">
        </div>
    </section>
</template>
<script setup>
import spotify from "@/assets/images/spotify.svg"
import dropbox from "@/assets/images/dropbox.svg"
import slack from "@/assets/images/slack.svg"
import zoom from "@/assets/images/zoom.svg"
</script>
<style scoped></style>