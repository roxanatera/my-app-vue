<template>
  <footer class="bg-gray-800 text-white mt-12">
    <div class="max-w-6xl mx-auto px-4 py-10 grid grid-cols-1 md:grid-cols-3 gap-8">

      <!-- Columna 1: Logo y descripción -->
      <div>
        <div class="flex items-center gap-2 mb-4">
          <img src="https://via.placeholder.com/40" alt="Logo" class="w-10 h-10">
          <h2 class="text-xl font-bold">Mi App</h2>
        </div>
        <p class="text-gray-400 text-sm">
          Proyecto de prueba con Vue 3 + TailwindCSS.
          Construido para practicar componentes y diseño responsive.
        </p>
      </div>

      <!-- Columna 2: Navegación -->
      <div>
        <h3 class="text-lg font-semibold mb-4">Dónde estamos</h3>
        <ul class="space-y-2 text-gray-300">
          <li><a href="#" class="hover:text-white transition-colors">Inicio</a></li>
          <li><a href="#" class="hover:text-white transition-colors">Productos</a></li>
          <li><a href="#" class="hover:text-white transition-colors">Contacto</a></li>
        </ul>
      </div>

      <!-- Columna 3: Redes sociales -->
      <div>
        <h3 class="text-lg font-semibold mb-4">Síguenos</h3>
        <div class="flex gap-4">
          <!-- Facebook -->
          <a href="https://facebook.com" target="_blank" class="text-gray-400 hover:text-white transition-colors">
            <svg class="w-6 h-6" fill="currentColor" viewBox="0 0 24 24">
              <path d="M22 12a10 10 0 1 0-11.5 9.9v-7h-2v-3h2v-2c0-2 1.2-3.2 3-3.2.9 0 1.8.1 1.8.1v2h-1c-1 0-1.3.6-1.3 1.2v1.9h2.5l-.4 3h-2.1v7A10 10 0 0 0 22 12"></path>
            </svg>
          </a>
          <!-- Twitter -->
          <a href="https://twitter.com" target="_blank" class="text-gray-400 hover:text-white transition-colors">
            <svg class="w-6 h-6" fill="currentColor" viewBox="0 0 24 24">
              <path d="M22.46 6c-.77.35-1.6.59-2.46.7a4.28 4.28 0 0 0 1.88-2.37 8.59 8.59 0 0 1-2.72 1.04 4.27 4.27 0 0 0-7.29 3.9A12.12 12.12 0 0 1 3.16 4.9a4.27 4.27 0 0 0 1.32 5.7 4.21 4.21 0 0 1-1.94-.54v.05a4.27 4.27 0 0 0 3.43 4.18 4.3 4.3 0 0 1-1.93.07 4.27 4.27 0 0 0 3.99 2.97A8.56 8.56 0 0 1 2 19.54a12.07 12.07 0 0 0 6.56 1.92c7.88 0 12.2-6.53 12.2-12.2v-.56c.84-.6 1.56-1.34 2.14-2.2z"></path>
            </svg>
          </a>
          <!-- GitHub -->
          <a href="https://github.com" target="_blank" class="text-gray-400 hover:text-white transition-colors">
            <svg class="w-6 h-6" fill="currentColor" viewBox="0 0 24 24">
              <path fill-rule="evenodd" d="M12 2C6.48 2 2 6.58 2 12.18c0 4.48 2.87 8.28 6.84 9.63.5.1.68-.22.68-.48v-1.68c-2.78.61-3.37-1.36-3.37-1.36-.46-1.18-1.13-1.5-1.13-1.5-.92-.64.07-.63.07-.63 1.01.07 1.54 1.06 1.54 1.06.9 1.56 2.36 1.11 2.93.85.09-.67.35-1.11.63-1.37-2.22-.26-4.56-1.13-4.56-5a3.91 3.91 0 0 1 1.05-2.7 3.63 3.63 0 0 1 .1-2.66s.84-.27 2.75 1.02a9.37 9.37 0 0 1 5 0c1.91-1.29 2.75-1.02 2.75-1.02.56 1.38.21 2.4.1 2.66a3.91 3.91 0 0 1 1.05 2.7c0 3.88-2.35 4.73-4.58 4.98.36.32.68.95.68 1.91v2.83c0 .27.18.59.69.48A10.19 10.19 0 0 0 22 12.18C22 6.58 17.52 2 12 2z" clip-rule="evenodd"/>
            </svg>
          </a>
        </div>
      </div>
    </div>

    <!-- Footer inferior -->
    <div class="border-t border-gray-700 py-4">
      <p class="text-center text-gray-400 text-sm">&copy; 2025 Mi App. Todos los derechos reservados.</p>
    </div>
  </footer>
</template>
