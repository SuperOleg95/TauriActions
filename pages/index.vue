<script setup lang="ts">

import { ask } from '@tauri-apps/plugin-dialog';
// when using `"withGlobalTauri": true`, you may use
// const { ask } = window.__TAURI__.dialog;

const askFunc = async () => {
// Create a Yes/No dialog
const answer = await ask('This action cannot be reverted. Are you sure?', {
  title: 'Tauri',
  kind: 'warning',
});
console.log(answer);
}

</script>

<template>
<button @click="askFunc">Click me</button>
</template>