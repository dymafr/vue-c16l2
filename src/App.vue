<template>
  <div class="p-20">
    <button class="btn btn-primary" @click="show = !show">Display</button>
    <Transition appear name="fade">
      <h1 v-if="show">Bonjour !</h1>
    </Transition>
  </div>
</template>

<script setup lang="ts">
import { ref } from 'vue';

const show = ref(true);
</script>

<style lang="scss">
@import './assets/scss/base.scss';

.fade-enter-from,
.fade-leave-to {
  opacity: 0;
}

.fade-enter-to,
.fade-leave-from {
  opacity: 1;
}

.fade-enter-active,
.fade-leave-active {
  transition: all 2s;
}
</style>
