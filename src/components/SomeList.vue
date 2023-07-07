<script setup lang="ts">
import { ref } from "vue";
import SomeObject from "./SomeObject.vue";
import IPerson from "../models/IPerson.ts";
import SomeForm from "./SomeForm.vue";

const persons = ref<IPerson[]>([{ name: "Vera", age: 40, hasPet: true }]);
</script>

<template>
  <!-- nästlad komponent  -->
  <div class="personWrapper">
    <SomeObject></SomeObject>
  </div>
  <SomeForm></SomeForm>
</template>

<style scoped></style>
