<script setup>
import { RouterView } from 'vue-router'
import { ref, onMounted, onUnmounted } from 'vue'

const dot = ref(null)
let lastTransform = ''

function onMove(e) {
  lastTransform = `translate(${e.clientX}px, ${e.clientY}px)`
  if (!dot.value) return

  const inNav = e.target.closest('nav') !== null
  const isButton = e.target.closest('button') !== null
  const isLink = e.target.closest('a') !== null

  const hideCursor = inNav || isButton || isLink

  dot.value.style.display = hideCursor ? 'none' : 'block'

  if (!hideCursor) {
    dot.value.style.transform = lastTransform
  }
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
    dot.value.style.transform = `translate(${window.innerWidth / 2}px, ${window.innerHeight / 2}px)`
  }
  window.addEventListener('pointermove', onMove)
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
:global(body) {
  cursor: none;
}

:global(nav, nav *, button, a) {
  cursor: initial;
}

.cursor-dot {
  position: fixed;
  left: 0;
  top: 0;
  width: 24px;
  height: 24px;
  border-radius: 50%;
  background: #833AB4;
  background: linear-gradient(90deg, rgba(131, 58, 180, 1) 0%, rgba(253, 29, 29, 1) 90%);
  pointer-events: none;
  transform: translate(-50%, -50%);
  transition: transform 0.07s linear;
  z-index: 9999;
  box-shadow: 0 0 8px rgba(255, 0, 0, 0.7);
}
</style>
