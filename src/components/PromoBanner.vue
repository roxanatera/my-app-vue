<script setup>
import { ref, onMounted, onBeforeUnmount } from 'vue'

const props = defineProps({
  slides: {
    type: Array,
    default: () => ([
      {
        title: '🎄 Ofertas de Navidad',
        text: 'Hasta -40% en selección',
        image: 'https://images.unsplash.com/photo-1512389142860-9c449e58a543?q=80&w=1600&auto=format&fit=crop'
      },
      {
        title: '🔥 2x1 en Accesorios',
        text: 'Solo esta semana',
        image: 'https://images.unsplash.com/photo-1542291026-7eec264c27ff?q=80&w=1600&auto=format&fit=crop'
      },
      {
        title: '🚚 Envío Gratis 24h',
        text: 'Pedidos +49€',
        image: 'https://images.unsplash.com/photo-1545235617-9465d2a55698?q=80&w=1600&auto=format&fit=crop'
      },
    ])
  },
  intervalMs: { type: Number, default: 4500 }
})

const idx = ref(0)
let t
const next = () => { idx.value = (idx.value + 1) % props.slides.length }
onMounted(() => { t = setInterval(next, props.intervalMs) })
onBeforeUnmount(() => clearInterval(t))
</script>

<template>
  <section class="relative w-full h-40 md:h-52 rounded-xl overflow-hidden shadow-md">
    <div v-for="(s,i) in slides" :key="i"
         class="absolute inset-0 transition-opacity duration-700"
         :class="i===idx ? 'opacity-100' : 'opacity-0'">
      <img :src="s.image" :alt="s.title" class="w-full h-full object-cover" />
      <div class="absolute inset-0 bg-gradient-to-r from-black/70 via-black/40 to-transparent"></div>
      <div class="absolute inset-0 backdrop-blur-[2px]"></div>
    </div>

    <div class="relative z-10 h-full flex items-center justify-between px-4 md:px-6 text-white">
      <div>
        <h3 class="text-lg md:text-2xl font-bold leading-tight drop-shadow">{{ slides[idx]?.title }}</h3>
        <p class="text-sm md:text-base text-white/90">{{ slides[idx]?.text }}</p>
        <div class="mt-2 flex gap-1.5">
          <span v-for="(s,i) in slides" :key="'dot-'+i"
                class="h-1.5 rounded-full transition-all"
                :class="i===idx ? 'w-6 bg-white' : 'w-2 bg-white/60'"></span>
        </div>
      </div>
      <a href="#"
         class="inline-flex items-center rounded-lg px-4 py-2 bg-blue-600 hover:bg-blue-700 text-white transition">
        Ver ofertas
      </a>
    </div>
  </section>
</template>
