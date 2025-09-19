<script setup>
defineProps({
  product: {
    type: Object,
    required: true
  }
})
</script>

<template>
  <!-- usamos group para que hover funcione en hijos -->
  <div class="group relative bg-white rounded-lg shadow-md overflow-hidden hover:shadow-lg transition-shadow">
    <!-- Imagen con efecto blur + zoom -->
    <img
      :src="product.image"
      :alt="product.name"
      class="w-full h-48 object-cover transition duration-500 ease-in-out group-hover:blur-sm group-hover:scale-105"
    >

    <!-- Overlay degradado al hover -->
    <div class="absolute inset-0 opacity-0 group-hover:opacity-100 transition duration-500
                bg-gradient-to-t from-black/70 via-black/40 to-transparent"></div>

    <!-- Contenido -->
    <div class="p-4 relative z-10">
      <h3 class="text-xl font-semibold text-gray-800 mb-2">{{ product.name }}</h3>
      <p class="text-gray-600 mb-4">{{ product.description }}</p>
      <div class="flex justify-between items-center">
        <span class="text-2xl font-bold text-green-600">${{ product.price }}</span>
        <button class="bg-green-500 hover:bg-green-600 text-white px-4 py-2 rounded-md transition-colors">
          Comprar
        </button>
      </div>
    </div>
  </div>
</template>

