<script setup>
const props = defineProps(["name"]);
const emit = defineEmits(["update:name"]);

const reverseText = () => {
  emit("update:name", props.name.split("").reverse().join(""));
};
</script>

<template>
  <div class="w-full max-w-md">
    <div class="md:flex md:items-center">
      <div class="md:w-1/3"></div>
      <div class="md:w-2/3">
        <button
          @click="reverseText()"
          class="shadow bg-purple-500 hover:bg-purple-400 focus:shadow-outline focus:outline-none text-white font-bold py-2 px-4 rounded"
          type="button"
        >
          Reverse Name
        </button>
      </div>
    </div>
  </div>
</template>

<style scoped>
</style>
