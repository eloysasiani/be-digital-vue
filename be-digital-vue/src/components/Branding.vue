<template>
    <section class="branding">
        <h2>Algumas empresas que confiam em nossos serviços:</h2>
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
<style scoped>
.container {
    display: grid;
    gap: 2rem;
    grid-template-rows: 1fr;
    grid-template-columns: repeat(4, 1fr);
}

.branding {
    display: grid;
    gap: 4rem;
}
</style>