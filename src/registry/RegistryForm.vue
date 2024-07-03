<script setup lang="ts">
import AppInput from '@/components/ui/AppInput.vue';
import RegistryItem from './RegistryItem.vue';
import { reactive, ref } from 'vue';

const formData = new FormData();
const RegisterForm = reactive({
  fullName: {
    title: "Full Name",
    value: "",
  },
  position: {
    title: "Position you are applying for",
    value: "",
  },
  email: {
    title: "Email",
    value: "",
  },
  phoneNumber: {
    title: "Phone number",
    value: "",
  },
  country: {
    title: "Country",
    value: "",
  },
  city: {
    title: "City",
    value: "",
  },
  password: {
    title: "Password",
    value: "",
  },
  confirmPassword: {
    title: "Confirm password",
    value: "",
  },
  gender: {
    title: "Gender",
    value: "",
  },
});
</script>

<template>
  <pre>{{ RegisterForm }}</pre>
  <form>
    <fieldset>
      <RegistryItem v-for="item in RegisterForm" :key="item.title" :title="item.title" editor="size">
        <template #title="{ title }">
          {{ title }}
        </template>
        <template #editor>
          <AppInput v-model="item.value" />
        </template>
      </RegistryItem>
    </fieldset>
  </form>
</template>