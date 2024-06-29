<script setup lang="ts">
import { ref } from 'vue';

defineProps<{ msg: string }>();

const textoRedes = ref('siguenos en facebook');
</script>

<template>
  <div class="container">
    <header>
      <slot name="header" :mensaje="msg"></slot>
    </header>
    <main>
      <slot></slot>
    </main>
    <footer>
      <slot name="footer" :redes="textoRedes"></slot>
    </footer>
  </div>
</template>

<style scoped></style>
