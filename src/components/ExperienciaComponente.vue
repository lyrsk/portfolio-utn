<script setup>
import { ref } from 'vue'
const titulo = 'Diseñadora UX/UI'
const fecha = 'Noviembre 2023 | Actualidad'
const experiencias = ref([
  {
    id: 1,
    parrafo:
      'Diseño de interfaces atractivas y funcionales, creación de experiencias de usuario optimizadas mediante investigación y pruebas de usabilidad, desarrollo de prototipos interactivos y adaptación de soluciones visuales que alineen objetivos de negocio con las necesidades del usuario.',
  },
])
</script>

<template>
  <div class="card">
    <h3 class="titulo">{{ titulo.toLocaleUpperCase() }}</h3>
    <p class="fecha">{{ fecha }}</p>
    <ul class="listado">
      <li class="item" v-for="experencia in experiencias" :key="experencia.id">
        <p>{{ experencia.parrafo }}</p>
      </li>
    </ul>
  </div>
</template>

<style scoped>
.card {
  display: flex;
  flex-direction: column;
  padding: 2rem;
  background-color: var(--black-secondary);
  border-radius: 15px;
  border: 1px solid var(--white-tertiary);
}

.fecha {
  margin-bottom: 1rem;
}

.listado {
  display: flex;
  flex-direction: column;
}

.item {
  align-items: center;
  display: flex;

  gap: 1.5rem;
}
</style>
