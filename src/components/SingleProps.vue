<script setup>
defineProps(["modelValue", "label"]);
// const emit = defineEmits(['update:modelValue']);

// const changeInput = (value) => {
//   emit('update:modelValue', value);
// }

</script>

<template>
  <div class="w-full max-w-md">
    <form class="w-full">
      <!-- <div class="md:flex md:items-center mb-6">
        <div class="md:w-1/3">
          <label
            class="block text-gray-500 font-bold md:text-right mb-1 md:mb-0 pr-4"
            for="inline-full-name"
          >
            {{ label }}
          </label>
        </div>
        <div class="md:w-2/3">
          <input
            :value="modelValue"
            @input="changeInput($event.target.value)"
            class="bg-gray-200 appearance-none border-2 border-gray-200 rounded w-full py-2 px-4 text-gray-700 leading-tight focus:outline-none focus:bg-white focus:border-purple-500"
            type="text"
          />
        </div>
      </div> -->
      <div class="md:flex md:items-center mb-6">
        <div class="md:w-1/3">
          <label
            class="block text-gray-500 font-bold md:text-right mb-1 md:mb-0 pr-4"
            for="inline-full-name"
          >
            {{ label }}
          </label>
        </div>
        <div class="md:w-2/3">
          <input
            :value="modelValue"
            @input="$emit('update:modelValue', $event.target.value)"
            class="bg-gray-200 appearance-none border-2 border-gray-200 rounded w-full py-2 px-4 text-gray-700 leading-tight focus:outline-none focus:bg-white focus:border-purple-500"
            type="text"
          />
        </div>
      </div>
    </form>
  </div>
</template>

<style scoped>
</style>
