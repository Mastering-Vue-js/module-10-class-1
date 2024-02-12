<script setup>
import { reactive, ref } from "vue";
import Child from "./components/Child.vue";
import SingleProps from "./components/SingleProps.vue";
import MultipleProps from "./components/MultipleProps.vue";
import ChildWithChild from "./components/ChildWithChild.vue";

const person = reactive({
  name: "John Doe",
  age: 35,
  occupation: "Vue.js Developer",
});
</script>

<template>
  <div class="w-full max-w-md">
    <h1 class="px-2 py-4">Parent Component</h1>
    <form class="w-full">
      <p class="px-2 py-4">
        Person Name: {{ person.name }}, Age: {{ person.age }} and Occupation:
        {{ person.occupation }}
      </p>
      <div class="md:flex md:items-center mb-6">
        <div class="md:w-1/3">
          <label
            class="block text-gray-500 font-bold md:text-right mb-1 md:mb-0 pr-4"
            for="inline-full-name"
          >
            Name
          </label>
        </div>
        <div class="md:w-2/3">
          <input
            v-model="person.name"
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
            Age
          </label>
        </div>
        <div class="md:w-2/3">
          <input
            v-model="person.age"
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
            Occupation
          </label>
        </div>
        <div class="md:w-2/3">
          <input
            v-model="person.occupation"
            class="bg-gray-200 appearance-none border-2 border-gray-200 rounded w-full py-2 px-4 text-gray-700 leading-tight focus:outline-none focus:bg-white focus:border-purple-500"
            type="text"
          />
        </div>
      </div>
    </form>
    <!-- <Child :person="person" />
    <SingleProps v-model="person.name" label="Name"/>
    <MultipleProps v-model:name="person.name" v-model:age="person.age"/> -->
    <ChildWithChild :person="person" />
  </div>
</template>

<style scoped>
</style>
