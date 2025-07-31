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
            <img :src="trophy" alt="" class="brand">
            <h2 id="counter-text">Mais de <span>0</span> prêmios</h2>
        </div>
        <div>
            <img :src="threestar" alt="" class="brand">
            <h2 id="counter2-text">Mais de <span>0</span> clientes satisfeitos</h2>
        </div>
        <div>
            <img :src="star" alt="" class="brand">
            <h2 id="counter3-text">Mais de <span>0</span> vistorias</h2>
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
    const animateCounter = (id, limit) => {
        let count = 1
        const el = document.querySelector(`#${id} span`)
        const interval = setInterval(() => {
            el.textContent = count
            count++
            if (count > limit) clearInterval(interval)
        }, 100)
    }

    animateCounter("counter-text", 25)
    animateCounter("counter2-text", 62)
    animateCounter("counter3-text", 47)
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



.more-about-us h2 {
    font-size: 1.4rem;
    color: aliceblue;
    font-weight: 800;
}

.more-about-us {
    display: flex;
    flex-direction: row;
    justify-content: space-around;
    padding: 4rem;
    border-radius: 2rem;
    background: #833AB4;
    background: linear-gradient(90deg, rgba(131, 58, 180, 1) 0%, rgba(253, 29, 29, 1) 50%, rgba(252, 176, 69, 1) 100%);

}

.more-about-us div {
    align-items: center;
    flex-direction: column;
    gap: 2rem;
    display: flex;
}


.more-about-us img {
    width: 14vh;
    animation: float 3s ease-in-out infinite;
}

@keyframes float {
    0% {
        transform: translateY(0px);
    }

    50% {
        transform: translateY(-10px);
    }

    100% {
        transform: translateY(0px);
    }
}

span {
    font-size: 3rem;
    font-family: Georgia, 'Times New Roman', Times, serif;
}
</style>
