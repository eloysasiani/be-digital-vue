<template>
       <div class="cards">

              <div class="conteudo">
                     <img :src="businessDeal" alt="">
                     <div class="text">
                            <h2>Branding & Design system</h2>
                            <p>Normalmente usado em indústrias gráficas e produtoras para pré-visualização de designs,
                                   layouts
                                   e mockups</p>
                            <svg width="48" height="40" viewBox="0 0 24 16" fill="none"
                                   xmlns="http://www.w3.org/2000/svg">
                                   <path d="M23.2493 8.70711C23.6398 8.31658 23.6398 7.68342 23.2493 7.29289L16.8853 0.928932C16.4948 0.538408 15.8616 0.538408 15.4711 0.928932C15.0806 1.31946 15.0806 1.95262 15.4711 2.34315L21.1279 8L15.4711 13.6569C15.0806 14.0474 15.0806 14.6805 15.4711 15.0711C15.8616 15.4616 16.4948 15.4616 16.8853 15.0711L23.2493 8.70711ZM0.313232 9H22.5421V7H0.313232V9Z"
                                          fill="#272D38" />
                            </svg>
                     </div>

              </div>


              <div class="conteudo">
                     <div class="text">
                            <h2>Análise de resultados</h2>
                            <p>Todo projeto de comunicação precisa de um objetivo bem definido. Ajudamos no
                                   acompanhamento dos resultados obtidos.</p>
                            <svg width="48" height="40" viewBox="0 0 24 16" fill="none"
                                   xmlns="http://www.w3.org/2000/svg">
                                   <path d="M23.2493 8.70711C23.6398 8.31658 23.6398 7.68342 23.2493 7.29289L16.8853 0.928932C16.4948 0.538408 15.8616 0.538408 15.4711 0.928932C15.0806 1.31946 15.0806 1.95262 15.4711 2.34315L21.1279 8L15.4711 13.6569C15.0806 14.0474 15.0806 14.6805 15.4711 15.0711C15.8616 15.4616 16.4948 15.4616 16.8853 15.0711L23.2493 8.70711ZM0.313232 9H22.5421V7H0.313232V9Z"
                                          fill="#272D38" />
                            </svg>
                     </div>
                     <img :src="businessManCheckingFinancialReport" alt="">

              </div>

       </div>
</template>
<script setup>
import businessManCheckingFinancialReport from "@/assets/images/businessman-checking-financial-report.png"
import businessDeal from "@/assets/images/business-deal.png"
</script>
<style scoped>
.cards {
       display: grid;
       grid-template-columns: 1fr;
       grid-gap: 20px;
       grid-template-rows: repeat(2, 1fr);
}

.conteudo {
       display: grid;
       grid-template-columns: repeat(2, 1fr);
}

.text {
       display: flex;
       flex-direction: column;
}

.text h2 {
       background: linear-gradient(90deg, rgba(131, 58, 180, 1) 0%, rgba(253, 29, 29, 1) 90%);
       -webkit-background-clip: text;
       background-clip: text;
       color: transparent;
       -webkit-text-fill-color: transparent;
       font-size: 5rem;

}
</style>