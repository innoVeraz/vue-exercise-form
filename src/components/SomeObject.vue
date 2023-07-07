<script setup lang="ts">
import { ref } from "vue";
import IPerson from "../models/IPerson.ts";

const person = ref<IPerson>({ name: "Vera", age: 40, hasPet: true });
const ageClass = "age";
</script>

<template>
  <div class="person">
    <!-- ternary för att sätta två klasser inom ett villkor -->
    <h3 :class="person.name === 'Vera' ? 'nameClass' : 'someOtherClass'">
      {{ person.name }}
    </h3>
    <p :class="{ age: person.age === 40 }">{{ person.age }}</p>
  </div>
</template>

<style scoped>
.age {
  color: rgb(218, 32, 153);
}
</style>
