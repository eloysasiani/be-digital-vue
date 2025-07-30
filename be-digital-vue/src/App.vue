<script setup>
import { RouterView } from 'vue-router'
import { ref, onMounted, onUnmounted } from 'vue'

const dot = ref(null)
let lastTransform = ''

function onMove(e) {
  lastTransform = `translate(${e.clientX}px, ${e.clientY}px)`
  if (!dot.value) return
  dot.value.style.transform = lastTransform     // => SEM esconder
  if (dot.value.style.display !== 'block') dot.value.style.display = 'block'
}

function onDown() {
  if (!dot.value) return
  dot.value.animate(
    [
      { transform: lastTransform + ' scale(1)' },
      { transform: lastTransform + ' scale(0.6)' },
      { transform: lastTransform + ' scale(1)' }
    ],
    { duration: 150, easing: 'ease-out' }
  )
}

onMounted(() => {
  if (dot.value) {
    // Posição inicial visível (centro do ecrã)
    dot.value.style.display = 'block'
    dot.value.style.transform = `translate(${window.innerWidth / 2}px, ${window.innerHeight / 2}px)`
  }
  window.addEventListener('pointermove', onMove, { passive: true })
  window.addEventListener('pointerdown', onDown)
})

onUnmounted(() => {
  window.removeEventListener('pointermove', onMove)
  window.removeEventListener('pointerdown', onDown)
})
</script>

<template>
  <RouterView />
  <div class="cursor-dot" ref="dot"></div>
</template>

<style scoped>
:global(html, body, *) {
  cursor: none !important;
}

:global(a),
:global(button),
:global([role="button"]) {
  cursor: none !important;
}

.cursor-dot {
  position: fixed;
  left: 0;
  top: 0;
  width: 34px;
  height: 34px;
  border-radius: 50%;
  background: linear-gradient(90deg, rgba(131, 58, 180, 1) 0%, rgba(253, 29, 29, 1) 90%);
  pointer-events: none;
  /* não bloqueia cliques/hover */
  transform: translate(-50%, -50%);
  transition: transform 0.07s linear;
  /* suaviza o movimento */
  z-index: 9999;
  box-shadow: 0 0 8px rgba(255, 0, 0, 0.7);
}
</style>
