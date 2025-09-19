# .

Proyecto de Prueba: Vue 3 + Vite + TailwindCSS 4

Este es un proyecto de prueba desarrollado con Vue 3, Vite y TailwindCSS v4.
Incluye ejemplos prácticos de componentes reutilizables: Cards, Grid de productos, Formulario de contacto, Alertas, Badges, Botones y Navegación con Tabs.

## Tecnologías utilizadas

Vue 3 (Composition API con <script setup>)

Vite como bundler ultrarrápido

TailwindCSS v4 para estilos utilitarios

ESLint + Prettier para linting y formateo

src/
  assets/
    tailwind.css        # Estilos globales con Tailwind
  components/
    AppHeader.vue
    AppFooter.vue
    ProductCard.vue
    ProductGrid.vue
    ContactForm.vue
    AlertsGroup.vue
    BadgesButtons.vue
    TabsNav.vue
  App.vue               # Componente raíz que orquesta todo
  main.js               # Punto de entrada de la aplicación

## Componentes principales

AppHeader / AppFooter → Cabecera y pie de página

ProductGrid + ProductCard → Renderizan una cuadrícula de productos

ContactForm → Formulario de contacto simple

AlertsGroup → Alertas de éxito, advertencia y error

BadgesButtons → Ejemplos de badges y botones con Tailwind

TabsNav → Navegación por pestañas con v-model

## Demostración

Aquí puedes ver un video de ejemplo del proyecto en ejecución:

👉 [Ver video de demostración:]
(https://youtube.com/shorts/5CsO6EC9kTU?feature=share)

📌 Notas

Proyecto creado únicamente con fines de aprendizaje/prueba

Perfecto como base para practicar Vue + Tailwind

Fácil de extender con vue-router y Pinia

## Customize configuration

See [Vite Configuration Reference](https://vite.dev/config/).

## Project Setup

```sh
npm install
```

### Compile and Hot-Reload for Development

```sh
npm run dev
```

### Compile and Minify for Production

```sh
npm run build
```

### Lint with [ESLint](https://eslint.org/)

```sh
npm run lint
```
