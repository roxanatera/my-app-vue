<script setup>
import { ref } from 'vue'
import AppHeader from './components/AppHeader.vue'
import ProductGrid from './components/ProductGrid.vue'
import ContactForm from './components/ContactForm.vue'
import AlertsGroup from './components/AlertsGroup.vue'
import BadgesButtons from './components/BadgesButtons.vue'
import TabsNav from './components/TabsNav.vue'
import AppFooter from './components/AppFooter.vue'

const activeTab = ref('home')

const products = [
  { id: 1, name: 'Producto 1', description: 'Descripción del producto 1', price: 29.99,
    image: 'https://via.placeholder.com/300x200/3B82F6/FFFFFF?text=Producto+1' },
  { id: 2, name: 'Producto 2', description: 'Descripción del producto 2', price: 39.99,
    image: 'https://via.placeholder.com/300x200/10B981/FFFFFF?text=Producto+2' },
  { id: 3, name: 'Producto 3', description: 'Descripción del producto 3', price: 49.99,
    image: 'https://via.placeholder.com/300x200/F59E0B/FFFFFF?text=Producto+3' },
]
</script>

<template>
  <div id="app" class="min-h-screen bg-gray-100">
    <AppHeader />

    <main class="max-w-6xl mx-auto px-4 py-8">
      <!-- Card simple -->
      <div class="bg-white rounded-lg shadow-md p-6 mb-8">
        <h2 class="text-2xl font-semibold text-gray-800 mb-4">Card con Tailwind</h2>
        <p class="text-gray-600 mb-4">
          Este es un ejemplo de una card usando clases de Tailwind CSS.
        </p>
        <button class="bg-blue-500 hover:bg-blue-700 text-white font-bold py-2 px-4 rounded">
          Click aquí
        </button>
      </div>

      <ProductGrid :products="products" />
      <ContactForm />
      <AlertsGroup />
      <BadgesButtons />
      <TabsNav v-model="activeTab" />
    </main>

    <AppFooter />
  </div>
</template>
