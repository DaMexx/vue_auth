<script setup>
import { useRouter } from 'vue-router';
const router = useRouter();
</script>

<template>
  <h1>This is an auth page</h1>
  <button @click="router.push('/registry')">is register already?</button>
</template>