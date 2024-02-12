<script setup>
import SingleProps from "./SingleProps.vue";
import ButtonModel from "./ButtonModel.vue";
defineProps(["person"]);
const emit = defineEmits(['update:modelValue']);
</script>

<template>
  <div class="w-full max-w-md">
    <h1 class="px-2 py-4">Child with child Component</h1>
    <form class="w-full">
      <SingleProps v-model="person.name" label="Name" />
      <SingleProps v-model="person.age" label="Age" />
      <SingleProps v-model="person.occupation" label="Occupation" />

      <ButtonModel v-model:name="person.name" />
    </form>
  </div>
</template>

<style scoped>
</style>
