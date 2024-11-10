<script setup>
import { ref } from 'vue'

const intereses = ref([
  'Dibujo y Diseño: Me apasiona crear ilustraciones y explorar nuevas técnicas de diseño, lo que me permite mantenerme en constante desarrollo creativo.',
  'Lectura y Escritura: Disfruto de la lectura, especialmente en temas de diseño y tecnología, y practico la escritura para expresar ideas y mejorar mis habilidades de comunicación.',
])
</script>

<template>
  <div class="intereses-contenedor">
    <FondoLava />
    <ul class="contenedor-lista">
      <li class="item" v-for="interes in intereses" :key="interes">
        {{ interes }}
      </li>
    </ul>
  </div>
</template>

<style scoped>
.intereses-contenedor {
  width: 100%;
  margin-top: 2rem;
  padding: 2rem 0;
  position: relative;
}

.contenedor-lista {
  display: flex;
  flex-wrap: wrap;
  justify-content: center;
  gap: 1rem;
  padding: 0;
  margin: 0;
}

.item {
  width: 100%;
  padding: 1rem;
  border: 1px solid var(--white-tertiary);
  border-radius: 8px;
  background-color: var(--black-secondary);
  color: var(--white-primary);
}

.item:nth-child(odd) {
  background-color: var(--black-primary);
}

.item:nth-child(even) {
  background-color: var(--black-secondary);
}

ul li {
  list-style: none;
}
</style>
