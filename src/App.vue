<!-- App.vue - Ejemplo completo -->
<template>
  <div id="app" class="min-h-screen bg-gray-100">
    <!-- Header -->
    <header class="bg-white shadow-sm">
      <div class="max-w-6xl mx-auto px-4 py-4">
        <h1 class="text-3xl font-bold text-gray-800">Mi App con Tailwind</h1>
      </div>
    </header>

    <!-- Contenido principal -->
    <main class="max-w-6xl mx-auto px-4 py-8">

      <!-- Ejemplo 1: Card simple -->
      <div class="bg-white rounded-lg shadow-md p-6 mb-8">
        <h2 class="text-2xl font-semibold text-gray-800 mb-4">Card con Tailwind</h2>
        <p class="text-gray-600 mb-4">Este es un ejemplo de una card usando clases de Tailwind CSS.</p>
        <button class="bg-blue-500 hover:bg-blue-700 text-white font-bold py-2 px-4 rounded">
          Click aquí
        </button>
      </div>

      <!-- Ejemplo 2: Grid de productos -->
      <div class="grid grid-cols-1 md:grid-cols-2 lg:grid-cols-3 gap-6 mb-8">
        <div v-for="product in products" :key="product.id"
             class="bg-white rounded-lg shadow-md overflow-hidden hover:shadow-lg transition-shadow">
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
      </div>

      <!-- Ejemplo 3: Formulario -->
      <div class="bg-white rounded-lg shadow-md p-6 mb-8">
        <h2 class="text-2xl font-semibold text-gray-800 mb-6">Formulario de Contacto</h2>
        <form class="space-y-4">
          <div>
            <label class="block text-sm font-medium text-gray-700 mb-2">Nombre</label>
            <input type="text"
                   class="w-full px-3 py-2 border border-gray-300 rounded-md focus:outline-none focus:ring-2 focus:ring-blue-500 focus:border-transparent">
          </div>
          <div>
            <label class="block text-sm font-medium text-gray-700 mb-2">Email</label>
            <input type="email"
                   class="w-full px-3 py-2 border border-gray-300 rounded-md focus:outline-none focus:ring-2 focus:ring-blue-500 focus:border-transparent">
          </div>
          <div>
            <label class="block text-sm font-medium text-gray-700 mb-2">Mensaje</label>
            <textarea rows="4"
                      class="w-full px-3 py-2 border border-gray-300 rounded-md focus:outline-none focus:ring-2 focus:ring-blue-500 focus:border-transparent"></textarea>
          </div>
          <button type="submit"
                  class="w-full bg-blue-500 hover:bg-blue-600 text-white font-medium py-2 px-4 rounded-md transition-colors">
            Enviar Mensaje
          </button>
        </form>
      </div>

      <!-- Ejemplo 4: Alertas -->
      <div class="space-y-4 mb-8">
        <div class="bg-green-100 border border-green-400 text-green-700 px-4 py-3 rounded relative">
          <strong class="font-bold">¡Éxito!</strong>
          <span class="block sm:inline"> Tu mensaje fue enviado correctamente.</span>
        </div>

        <div class="bg-yellow-100 border border-yellow-400 text-yellow-700 px-4 py-3 rounded relative">
          <strong class="font-bold">¡Atención!</strong>
          <span class="block sm:inline"> Revisa los campos del formulario.</span>
        </div>

        <div class="bg-red-100 border border-red-400 text-red-700 px-4 py-3 rounded relative">
          <strong class="font-bold">Error:</strong>
          <span class="block sm:inline"> No se pudo procesar tu solicitud.</span>
        </div>
      </div>

      <!-- Ejemplo 5: Badges y botones -->
      <div class="bg-white rounded-lg shadow-md p-6 mb-8">
        <h2 class="text-2xl font-semibold text-gray-800 mb-6">Badges y Botones</h2>

        <!-- Badges -->
        <div class="mb-6">
          <h3 class="text-lg font-medium text-gray-700 mb-3">Badges</h3>
          <div class="flex flex-wrap gap-2">
            <span class="bg-blue-100 text-blue-800 text-xs font-medium px-2.5 py-0.5 rounded">Nuevo</span>
            <span class="bg-green-100 text-green-800 text-xs font-medium px-2.5 py-0.5 rounded">En stock</span>
            <span class="bg-red-100 text-red-800 text-xs font-medium px-2.5 py-0.5 rounded">Agotado</span>
            <span class="bg-yellow-100 text-yellow-800 text-xs font-medium px-2.5 py-0.5 rounded">Destacado</span>
          </div>
        </div>

        <!-- Botones -->
        <div>
          <h3 class="text-lg font-medium text-gray-700 mb-3">Botones</h3>
          <div class="flex flex-wrap gap-4">
            <button class="bg-blue-500 hover:bg-blue-600 text-white px-4 py-2 rounded-md">Primario</button>
            <button class="bg-gray-500 hover:bg-gray-600 text-white px-4 py-2 rounded-md">Secundario</button>
            <button class="border border-blue-500 text-blue-500 hover:bg-blue-500 hover:text-white px-4 py-2 rounded-md transition-colors">
              Outline
            </button>
            <button class="text-blue-500 hover:text-blue-600 px-4 py-2">Solo texto</button>
          </div>
        </div>
      </div>

      <!-- Ejemplo 6: Navegación con tabs -->
      <div class="bg-white rounded-lg shadow-md p-6">
        <div class="border-b border-gray-200">
          <nav class="-mb-px flex space-x-8">
            <a href="#"
               :class="activeTab === 'home' ? 'border-blue-500 text-blue-600' : 'border-transparent text-gray-500 hover:text-gray-700 hover:border-gray-300'"
               class="whitespace-nowrap py-2 px-1 border-b-2 font-medium text-sm"
               @click="activeTab = 'home'">
              Inicio
            </a>
            <a href="#"
               :class="activeTab === 'about' ? 'border-blue-500 text-blue-600' : 'border-transparent text-gray-500 hover:text-gray-700 hover:border-gray-300'"
               class="whitespace-nowrap py-2 px-1 border-b-2 font-medium text-sm"
               @click="activeTab = 'about'">
              Acerca de
            </a>
            <a href="#"
               :class="activeTab === 'contact' ? 'border-blue-500 text-blue-600' : 'border-transparent text-gray-500 hover:text-gray-700 hover:border-gray-300'"
               class="whitespace-nowrap py-2 px-1 border-b-2 font-medium text-sm"
               @click="activeTab = 'contact'">
              Contacto
            </a>
          </nav>
        </div>

        <div class="mt-4">
          <div v-if="activeTab === 'home'" class="text-gray-600">
            <h3 class="text-lg font-medium mb-2">Inicio</h3>
            <p>Contenido de la página de inicio.</p>
          </div>
          <div v-if="activeTab === 'about'" class="text-gray-600">
            <h3 class="text-lg font-medium mb-2">Acerca de</h3>
            <p>Información sobre nuestra empresa.</p>
          </div>
          <div v-if="activeTab === 'contact'" class="text-gray-600">
            <h3 class="text-lg font-medium mb-2">Contacto</h3>
            <p>Formas de ponerse en contacto con nosotros.</p>
          </div>
        </div>
      </div>

    </main>

    <!-- Footer -->
    <footer class="bg-gray-800 text-white mt-12">
      <div class="max-w-6xl mx-auto px-4 py-8">
        <p class="text-center">&copy; 2025 Mi App. Todos los derechos reservados.</p>
      </div>
    </footer>
  </div>
</template>

<script>
export default {
  name: 'App',
  data() {
    return {
      activeTab: 'home',
      products: [
        {
          id: 1,
          name: 'Producto 1',
          description: 'Descripción del producto 1',
          price: 29.99,
          image: 'https://via.placeholder.com/300x200/3B82F6/FFFFFF?text=Producto+1'
        },
        {
          id: 2,
          name: 'Producto 2',
          description: 'Descripción del producto 2',
          price: 39.99,
          image: 'https://via.placeholder.com/300x200/10B981/FFFFFF?text=Producto+2'
        },
        {
          id: 3,
          name: 'Producto 3',
          description: 'Descripción del producto 3',
          price: 49.99,
          image: 'https://via.placeholder.com/300x200/F59E0B/FFFFFF?text=Producto+3'
        }
      ]
    }
  }
}
</script>
