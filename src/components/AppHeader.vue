<script setup>
import { ref } from 'vue'

const isOpen = ref(false)
</script>

<template>
  <header class="bg-white shadow-sm">
    <div class="max-w-6xl mx-auto px-4 py-4 flex justify-between items-center">
      <!-- Logo + título -->
      <div class="flex items-center gap-3">
        <img src="https://via.placeholder.com/40" alt="Logo" class="w-10 h-10">
        <h1 class="text-2xl font-bold text-gray-800">Mi App con Tailwind</h1>
      </div>

      <!-- Navegación Desktop -->
      <nav class="hidden md:flex gap-6">
        <a href="#" class="text-gray-600 hover:text-blue-600 transition-colors">Inicio</a>
        <a href="#" class="text-gray-600 hover:text-blue-600 transition-colors">Productos</a>
        <a href="#" class="text-gray-600 hover:text-blue-600 transition-colors">Contacto</a>
      </nav>

      <!-- Botón Desktop -->
      <div class="hidden md:block">
        <button class="bg-blue-500 hover:bg-blue-600 text-white px-4 py-2 rounded-md">
          Iniciar sesión
        </button>
      </div>

      <!-- Botón Hamburguesa (solo móvil) -->
      <button
        @click="isOpen = !isOpen"
        class="md:hidden inline-flex items-center justify-center p-2 rounded-md text-gray-600 hover:text-blue-600 hover:bg-gray-100 focus:outline-none"
      >
        <svg class="h-6 w-6" xmlns="http://www.w3.org/2000/svg" fill="none" viewBox="0 0 24 24" stroke="currentColor">
          <path v-if="!isOpen" stroke-linecap="round" stroke-linejoin="round" stroke-width="2"
            d="M4 6h16M4 12h16M4 18h16" />
          <path v-else stroke-linecap="round" stroke-linejoin="round" stroke-width="2"
            d="M6 18L18 6M6 6l12 12" />
        </svg>
      </button>
    </div>

    <!-- Menú desplegable móvil -->
    <div v-if="isOpen" class="md:hidden bg-white border-t border-gray-200">
      <nav class="flex flex-col px-4 py-4 space-y-2">
        <a href="#" class="text-gray-600 hover:text-blue-600 transition-colors">Inicio</a>
        <a href="#" class="text-gray-600 hover:text-blue-600 transition-colors">Productos</a>
        <a href="#" class="text-gray-600 hover:text-blue-600 transition-colors">Contacto</a>
        <button class="bg-blue-500 hover:bg-blue-600 text-white px-4 py-2 rounded-md">
          Iniciar sesión
        </button>
      </nav>
    </div>
  </header>
</template>
