<template>
  <footer class="principal">
    <div class="iniciofooter">
      <div class="textofooter">
        <h3>{{ typedText }}</h3>
        <p>Building digital products, brands & experience</p>
      </div>
      <div class="svg">
        <svg width="271" height="36" viewBox="0 0 271 36" fill="none" xmlns="http://www.w3.org/2000/svg">
          <!-- (o conteúdo SVG permanece o mesmo) -->
        </svg>
      </div>
    </div>

    <div class="finalfooter">
      <div class="info-contato">
        <h3>Contato:</h3>
        <p>contato@serdigital.com</p>
        <p>(11) 1234-5678</p>
      </div>
      <div class="footer_copy">
        <p>© Todos os direitos reservados</p>
      </div>
    </div>
  </footer>
</template>

<script setup>
import { ref, onMounted } from 'vue'

const texto = "SER DIGITAL"
const typedText = ref('')
const delay = 100

onMounted(() => {
  const letras = texto.split('')
  letras.forEach((letra, indice) => {
    setTimeout(() => {
      typedText.value += letra
    }, delay * indice)
  })
})
</script>

<style scoped>
.principal {
  color: white;
  border-radius: 2rem 2rem 0rem 0rem;
  padding: 2rem;
  font-family: 'Gill Sans', 'Gill Sans MT', Calibri, 'Trebuchet MS', sans-serif;
  background: linear-gradient(90deg, rgba(131, 58, 180, 1) 0%, rgba(253, 29, 29, 1) 50%, rgba(252, 176, 69, 1) 100%);
  margin: 0;
}

svg {
  filter: brightness(0) invert(1);
  display: block; /* Remove espaçamento vertical extra */
}

.principal p,
.principal h3 {
  margin: 0;
  padding: 0;
}

.footer_copy {
  text-align: center;
}

.iniciofooter {
  display: grid;
  grid-template-columns: repeat(2, 1fr);
  align-items: center;
  gap: 0;
}

.iniciofooter > div {
  margin: 0;
  padding: 0;
}

.textofooter {
  display: flex;
  flex-direction: column;
  justify-content: center;
}

.svg {
  display: flex;
  justify-content: flex-end;
}

.finalfooter {
  display: flex;
  justify-content: start;
  margin-top: 1rem;
}

.info-contato p {
  margin: 0;
}

.iniciofooter h3 {
  font-weight: 800;
  text-transform: uppercase;
  font-size: 1.5rem;
  margin-bottom: 0.5rem;
}
</style>
