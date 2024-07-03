<script setup lang="ts">

// defineSlots({
//   default: () => 'default',

// })
interface Props {
  title: string,
  editor: String,
}

defineProps<Props>();

</script>
<template>
  <p>
    <slot></slot>
    <slot name="title" :title="title"></slot>
    <slot name="editor"></slot>
  </p>
</template>