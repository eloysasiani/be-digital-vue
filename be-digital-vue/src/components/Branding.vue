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

    <section class="more-about-us">
        <div>
            <img :src="trophy" alt="" class="firstimage">
            <h2 id="counter-text">Mais de 0 prêmios</h2>
        </div>
        <div>
            <img :src="threestar" alt="" class="secondimage">
            <h2 id="counter2-text">Mais de 0 clientes satisfeitos</h2>
        </div>
        <div>
            <img :src="star" alt="" class="otherimage">
            <h2 id="counter3-text">Mais de 0 vistorias</h2>
        </div>
    </section>
</template>

<script setup>
import { onMounted } from 'vue'
import spotify from "@/assets/images/spotify.svg"
import dropbox from "@/assets/images/dropbox.svg"
import slack from "@/assets/images/slack.svg"
import zoom from "@/assets/images/zoom.svg"
import star from "@/assets/images/star.png"
import trophy from "@/assets/images/gold-thropy.png"
import threestar from "@/assets/images/three-star-rating.png"

onMounted(() => {
    const animateCounter = (id, limit, text) => {
        let count = 1
        const el = document.getElementById(id)
        const interval = setInterval(() => {
            el.textContent = `Mais de ${count} ${text}`
            count++
            if (count > limit) clearInterval(interval)
        }, 100)
    }

    animateCounter("counter-text", 25, "prêmios")
    animateCounter("counter2-text", 62, "clientes satisfeitos")
    animateCounter("counter3-text", 47, "vistorias")
})
</script>

<style scoped>
.container {
    display: flex;
    gap: 10rem;
    justify-content: space-around;
    padding: 2rem;
    border-radius: 1rem;
    background: linear-gradient(90deg, rgba(131, 58, 180, 1) 0%, rgb(173, 10, 10) 90%);
}

.branding {
    display: grid;
    gap: 4rem;
    background: linear-gradient(90deg, rgba(2, 0, 36, 1) 0%, rgba(9, 9, 121, 1) 35%, rgba(0, 212, 255, 1) 100%);
    padding: 4rem;
    color: white;
    border-radius: 2rem;
}

.more-about-us img {
    width: 12vh;
}

.more-about-us h2 {
    font-size: 1.4rem;
}

.more-about-us {
    display: flex;
    flex-direction: row;
    justify-content: space-around;
    background: #2A7B9B;
    background: #2A7B9B;
    background: linear-gradient(90deg, rgba(42, 123, 155, 1) 0%, rgba(8, 53, 117, 1) 50%, rgba(111, 237, 83, 1) 100%);

}
</style>
