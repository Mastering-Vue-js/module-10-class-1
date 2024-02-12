<script setup>
defineProps(["name", "age"]);
</script>

<template>
  <div class="w-full max-w-md">
    <h1 class="px-2 py-4">Single Input Component</h1>
    <form class="w-full">
      <div class="md:flex md:items-center mb-6">
        <div class="md:w-1/3">
          <label
            class="block text-gray-500 font-bold md:text-right mb-1 md:mb-0 pr-4"
            for="inline-full-name"
          >
            Label
          </label>
        </div>
        <div class="md:w-2/3">
          <input
            :value="name"
            @input="$emit('update:name', $event.target.value)"
            class="bg-gray-200 appearance-none border-2 border-gray-200 rounded w-full py-2 px-4 text-gray-700 leading-tight focus:outline-none focus:bg-white focus:border-purple-500"
            type="text"
          />
        </div>
      </div>
      <div class="md:flex md:items-center mb-6">
        <div class="md:w-1/3">
          <label
            class="block text-gray-500 font-bold md:text-right mb-1 md:mb-0 pr-4"
            for="inline-full-name"
          >
            Label
          </label>
        </div>
        <div class="md:w-2/3">
          <input
            :value="age"
            @input="$emit('update:age', $event.target.value)"
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
