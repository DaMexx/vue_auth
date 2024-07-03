<script setup lang="ts">
const value = defineModel()
interface Props {
  type?: string
}

const { type = 'text', ...props } = defineProps<Props>();

</script>

<template>
  <input type v-model="value">
</template>