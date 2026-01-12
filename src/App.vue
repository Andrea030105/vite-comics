<script setup>
import AppHeader from './components/AppHeader.vue'
import AppCenter from './components/AppCenter.vue';
import AppFooter from './components/AppFooter.vue';
</script>
<template>
  <div>
    <AppHeader />
    <AppCenter />
    <AppFooter />
  </div>
</template>
<style lang="scss">
@use './styles/generals.scss' as *;
</style>