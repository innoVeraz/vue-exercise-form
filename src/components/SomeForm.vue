<script setup lang="ts">
import { ref } from "vue";
import IPerson from "../models/IPerson";

const person = ref<IPerson>({ name: "", age: 0, hasPet: true });
const handleSubmit = () => {
  console.log("hantera", person.value);
};
</script>

<template>
  <form @submit.prevent="handleSubmit">
    <p>Namn</p>
    <input type="text" v-model="person.name" />
    <p>Ålder</p>
    <input type="number" v-model.number="person.age" />
    <p>Har husdjur</p>
    <input type="checkbox" v-model="person.hasPet" />
    <br />
    <button type="submit">spara</button>
  </form>
</template>

<style scoped></style>
