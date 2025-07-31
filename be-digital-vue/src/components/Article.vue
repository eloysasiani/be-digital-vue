<template>
       <div class="cards">
              <div class="conteudo">
                     <img :src="businessDeal" alt="">
                     <div class="text">
                            <h2>{{ typedText }}</h2>
                            <p>
                                   Normalmente usado em indústrias gráficas e produtoras para pré-visualização de
                                   designs,
                                   layouts e mockups.
                            </p>
                            <svg width="48" height="40" viewBox="0 0 24 16" fill="none"
                                   xmlns="http://www.w3.org/2000/svg">
                                   <path d="M23.2493 8.70711C23.6398 8.31658 23.6398 7.68342 23.2493 7.29289L16.8853 0.928932C16.4948 0.538408 15.8616 0.538408 15.4711 0.928932C15.0806 1.31946 15.0806 1.95262 15.4711 2.34315L21.1279 8L15.4711 13.6569C15.0806 14.0474 15.0806 14.6805 15.4711 15.0711C15.8616 15.4616 16.4948 15.4616 16.8853 15.0711L23.2493 8.70711ZM0.313232 9H22.5421V7H0.313232V9Z"
                                          fill="#272D38" />
                            </svg>
                     </div>
              </div>

              <div class="conteudo">
                     <div class="text">
                            <h2>{{ otherTypedText }}</h2>
                            <p>
                                   Todo projeto de comunicação precisa de um objetivo bem definido. Ajudamos no
                                   acompanhamento dos resultados obtidos.
                            </p>
                            <a href="#">
                                   <svg width="48" height="40" viewBox="0 0 24 16" fill="none"
                                          xmlns="http://www.w3.org/2000/svg">
                                          <path d="M23.2493 8.70711C23.6398 8.31658 23.6398 7.68342 23.2493 7.29289L16.8853 0.928932C16.4948 0.538408 15.8616 0.538408 15.4711 0.928932C15.0806 1.31946 15.0806 1.95262 15.4711 2.34315L21.1279 8L15.4711 13.6569C15.0806 14.0474 15.0806 14.6805 15.4711 15.0711C15.8616 15.4616 16.4948 15.4616 16.8853 15.0711L23.2493 8.70711ZM0.313232 9H22.5421V7H0.313232V9Z"
                                                 fill="#272D38" />
                                   </svg>
                            </a>
                     </div>
                     <img :src="businessManCheckingFinancialReport" alt="">
              </div>
       </div>
</template>

<script setup>
import { ref, onMounted } from 'vue'
import businessManCheckingFinancialReport from "@/assets/images/businessman-checking-financial-report.png"
import businessDeal from "@/assets/images/business-deal.png"

const typedText = ref('')
const otherTypedText = ref('')
const delay = 40

onMounted(() => {
       const firstText = "Branding & Design System"
       const secondText = "Análise de resultados"

       firstText.split("").forEach((letra, indice) => {
              setTimeout(() => {
                     typedText.value += letra
              }, delay * indice)
       })

       secondText.split("").forEach((letra, indice) => {
              setTimeout(() => {
                     otherTypedText.value += letra
              }, delay * indice + delay * firstText.length + 200) // espera o 1º terminar + 200ms
       })
})
</script>
<style scoped>
.cards {
       display: grid;
       grid-template-columns: 1fr;
       grid-gap: 20px;
       grid-template-rows: repeat(2, 1fr);
}

.conteudo {
       flex-direction: row;
       justify-content: space-around;
       gap: 30rem;
       display: flex;
       background: #c670ff;
       padding: 1.5rem;
       border-radius: 2rem;
       border: solid purple;
       background: linear-gradient(90deg, rgb(205, 170, 228) 0%, rgb(255, 255, 255) 50%);
}

.cards .conteudo:nth-last-child(1):hover {
       background: #755ed971;

}

.conteudo:hover {
       background: #755ed971;

}

.cards .conteudo:nth-last-child(1) {
       background: linear-gradient(90deg, rgb(255, 255, 255) 50%, rgb(205, 170, 228) 100%);

}


.conteudo img {
       width: 35vh;
}

.text {
       display: flex;
       flex-direction: column;
       gap: 2rem;
       align-self: center;
}

.text h2 {
       background: linear-gradient(90deg, rgba(131, 58, 180, 1) 0%, rgba(253, 29, 29, 1) 90%);
       -webkit-background-clip: text;
       background-clip: text;
       color: transparent;
       -webkit-text-fill-color: transparent;
       font-size: 3rem;

}

p {
       font-size: 1.2rem;

}

svg {
       animation: slideAndPulse 2s ease-in-out infinite;
       transform-origin: center;
}


@keyframes slideAndPulse {
       0% {
              transform: translateX(0px) scale(1);
              opacity: 0.7;
       }

       50% {
              transform: translateX(5px) scale(1.1);
              opacity: 1;
       }

       100% {
              transform: translateX(0px) scale(1);
              opacity: 0.7;
       }
}
</style>