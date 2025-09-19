<script setup>
defineProps({
  product: {
    type: Object,
    required: true
  }
})
</script>

<template>
  <div class="bg-white rounded-lg shadow-md overflow-hidden hover:shadow-lg transition-shadow">
    <img :src="product.image" :alt="product.name" class="w-full h-48 object-cover">
    <div class="p-4">
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
