<template>
  <div class="p-20">
    <button class="btn btn-primary" @click="show = !show">Display</button>
    <h1 v-if="show">Hello World !</h1>
  </div>
</template>

<script setup lang="ts">
import { ref } from 'vue';

const show = ref(false);
</script>

<style lang="scss">
@import './assets/scss/base.scss';
</style>
