<template>
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
</template>
