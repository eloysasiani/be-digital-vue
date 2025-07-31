<template>
    <div class="principal">
        <h2>O que os clientes dizem-nos:</h2>
        <div class="col1">
            <div class="col_card">
                <img :src="westernMan1" alt="">
                <span>Andrew Rathore</span>

                <p>Lorem ipsum dolor sit amet, consectetur adipiscing elit. Nunc ullamcorper scelerisque mi, in
                    malesuada
                    felis malesuada vel. </p>
                <img :src="fivestars" alt="" class="fivestars">
            </div>
            <div class="col_card">
                <img :src="westernMan2" alt="">
                <span>Vera Duncan</span>

                <p>Lorem ipsum dolor sit amet, consectetur adipiscing elit. Nunc ullamcorper scelerisque mi, in
                    malesuada
                    felis malesuada vel. </p>
                <img :src="fivestars" alt="" class="fivestars">
            </div>
            <div class="col_card">
                <img :src="westernMan3" alt="">
                <span>Mark Smith</span>

                <p>Lorem ipsum dolor sit amet, consectetur adipiscing elit. Nunc ullamcorper scelerisque mi, in
                    malesuada
                    felis malesuada vel. </p>
                <img :src="fivestars" alt="" class="fivestars">
            </div>
        </div>
    </div>

</template>
<script setup>
import westernMan1 from "@/assets/images/western-man-4975942-4159828-1-2x.png"
import westernMan2 from "@/assets/images/western-man-4975942-4159828-2-2x.png"
import westernMan3 from "@/assets/images/western-man-4975942-4159828-3-2x.png"
import fivestars from "@/assets/images/five-star-rating.png"
</script>
<style scoped>
.col1 {
    display: grid;
    grid-template-columns: repeat(3, 1fr);
    grid-row: 1fr;
    gap: 4rem;

}

.fivestars {
    width: 15vh;
}

.col_card {
    display: flex;
    flex-direction: column;
    align-items: center;
    justify-content: center;
    text-align: center;
    gap: 1rem;
    background-color: rgba(178, 178, 178, 0.105);
    padding-top: 3.5rem;
    border-radius: 2rem;
    border: solid 4px purple;
    transition: transform 0.3s ease;
}

.col_card:hover {
    transform: scale(1.05);
}

span {
    font-size: 1.3rem;
    background: linear-gradient(90deg, rgba(131, 58, 180, 1) 0%, rgba(253, 29, 29, 1) 90%);
    -webkit-background-clip: text;
    background-clip: text;
    color: transparent;
    -webkit-text-fill-color: transparent;
}

.principal {
    background: #020024;
    background: linear-gradient(90deg, rgba(2, 0, 36, 1) 0%, rgba(9, 9, 121, 1) 35%, rgba(0, 212, 255, 1) 100%);
    gap: 5rem;
    border-radius: 2rem;
}

img {
    width: 20vh;

}

p {
    width: 40vh;
    color: aliceblue;
}

h2 {
    margin: 0 auto;
    font-weight: 800;
    font-size: 2.3rem;
    color: aliceblue;
}
</style>