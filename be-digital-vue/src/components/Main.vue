<template>
    <div class="maior">

        <div class="text">
            <h2>Faça parte de algo grande</h2>
        </div>

        <div class="image">
            <img :src="customerSupport" alt="" class="suport">
        </div>

        <div class="text">

            <h3>Estamos aqui para ajudar-te</h3>
            <p>Nós trabalhamos com empresas de qualquer tamanho e estamos preparados para atender a sua
                necessidade.
                <a href="#"><button>Entre em Contato</button></a>
            </p>


        </div>
    </div>
</template>
<script setup>
import customerSupport from "@/assets/images/customer-support.png"
import hands from "@/assets/images/fist-bump-gesture.png"
</script>
<style scoped>
.maior {
    display: flex;
    justify-content: space-evenly;
    align-items: center;
    gap: 2rem;
    padding: 3rem 2rem;
    margin: 0 auto;
    background: linear-gradient(90deg, rgba(2, 0, 36, 1) 0%, rgba(9, 9, 121, 1) 35%, rgba(0, 212, 255, 1) 100%);
    border-radius: 2rem;
}




.image {
    display: flex;
    flex-direction: column;
}

.suport {
    width: 50vh;
}

h2 {
    text-align: center;
    background: linear-gradient(90deg, rgba(131, 58, 180, 1) 0%, rgba(253, 29, 29, 1) 90%);
    -webkit-background-clip: text;
    background-clip: text;
    color: transparent;
    -webkit-text-fill-color: transparent;
    font-size: 3rem;

}


.text {
    display: flex;
    flex-direction: column;
    justify-content: center;
    align-items: start;
    gap: 1rem;

}

.maior {
    background: #020024;
    border-radius: 2rem;
    padding: 3rem;
    background: linear-gradient(90deg, rgba(2, 0, 36, 1) 0%, rgba(9, 9, 121, 1) 35%, rgba(0, 212, 255, 1) 100%);
}

button {
    border: solid 2px rgb(254, 190, 255);
    margin-top: 1rem;
}

h3 {
    background: linear-gradient(90deg, rgba(131, 58, 180, 1) 0%, rgba(253, 29, 29, 1) 90%);
    -webkit-background-clip: text;
    background-clip: text;
    color: transparent;
    -webkit-text-fill-color: transparent;
    align-items: center;
    text-align: center;
    justify-content: center;
    margin: 0;
    font-size: 2.3rem;

}


p {
    font-size: 1.3rem;
    color: aliceblue;
    width: 55vh;
}

.text {
    display: flex;
    flex-direction: column;
    line-height: 2.2rem;

}
</style>