<script setup>
const props = defineProps({
  modelValue: {
    type: String,
    required: true
  }
})
const emit = defineEmits(['update:modelValue'])
const setTab = (t) => emit('update:modelValue', t)
</script>

<template>
  <div class="bg-white rounded-lg shadow-md p-6">
    <div class="border-b border-gray-200">
      <nav class="-mb-px flex space-x-8">
        <a href="#"
           :class="modelValue === 'home' ? 'border-blue-500 text-blue-600' : 'border-transparent text-gray-500 hover:text-gray-700 hover:border-gray-300'"
           class="whitespace-nowrap py-2 px-1 border-b-2 font-medium text-sm"
           @click.prevent="setTab('home')">
          Inicio
        </a>
        <a href="#"
           :class="modelValue === 'about' ? 'border-blue-500 text-blue-600' : 'border-transparent text-gray-500 hover:text-gray-700 hover:border-gray-300'"
           class="whitespace-nowrap py-2 px-1 border-b-2 font-medium text-sm"
           @click.prevent="setTab('about')">
          Acerca de
        </a>
        <a href="#"
           :class="modelValue === 'contact' ? 'border-blue-500 text-blue-600' : 'border-transparent text-gray-500 hover:text-gray-700 hover:border-gray-300'"
           class="whitespace-nowrap py-2 px-1 border-b-2 font-medium text-sm"
           @click.prevent="setTab('contact')">
          Contacto
        </a>
      </nav>
    </div>

    <div class="mt-4 text-gray-600">
      <div v-if="modelValue === 'home'">
        <h3 class="text-lg font-medium mb-2">Inicio</h3>
        <p>Contenido de la página de inicio.</p>
      </div>
      <div v-else-if="modelValue === 'about'">
        <h3 class="text-lg font-medium mb-2">Acerca de</h3>
        <p>Información sobre nuestra empresa.</p>
      </div>
      <div v-else>
        <h3 class="text-lg font-medium mb-2">Contacto</h3>
        <p>Formas de ponerse en contacto con nosotros.</p>
      </div>
    </div>
  </div>
</template>
