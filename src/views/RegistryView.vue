<script setup>
import { useRouter } from 'vue-router';
import AppInput from '@/components/ui/AppInput.vue';
import RegistryItem from '@/registry/RegistryItem.vue';
import RegistryForm from '@/registry/RegistryForm.vue';
const router = useRouter();


</script>

<template>
  <h1>Registration</h1>

  <RegistryForm></RegistryForm>
</template>