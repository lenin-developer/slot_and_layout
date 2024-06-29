<script setup lang="ts">
import LayoutMain from './components/LayoutMain.vue';
import ButtonSlot from './components/ButtonSlot.vue';
import MyIcon from './components/MyIcon.vue';
</script>

<template>
  <div>
    <a href="https://vuejs.org/" target="_blank">
      <img src="./assets/vue.svg" class="logo vue" alt="Vue logo" />
    </a>
  </div>

  <ButtonSlot> hola un texto </ButtonSlot>
  <ButtonSlot>
    <span>soy un span</span>
    <MyIcon />
  </ButtonSlot>

  <LayoutMain msg="saludoos">
    <template #header="headerProps">
      <h1>header , {{ headerProps.mensaje }}</h1>
    </template>

    <template #default>
      <h1>default</h1>
    </template>

    <template #footer="propsFooter">
      <h1>footer {{ propsFooter.redes }}</h1>
    </template>
  </LayoutMain>
</template>

<style scoped>
.logo {
  height: 6em;
  padding: 1.5em;
  will-change: filter;
  transition: filter 300ms;
}
.logo:hover {
  filter: drop-shadow(0 0 2em #646cffaa);
}
.logo.vue:hover {
  filter: drop-shadow(0 0 2em #42b883aa);
}
</style>
