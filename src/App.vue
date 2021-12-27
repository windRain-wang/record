<script setup lang="ts">
import {
  throttleFilter,
  useLocalStorage,
  useMouse,
  usePreferredDark,
} from "@vueuse/core";
const { x, y } = useMouse();
const isDark = usePreferredDark();
console.log(isDark.value);
isDark.value = true;
console.log(isDark.value);

const store = useLocalStorage(
  "my-storange",
  { name: "Apple", color: "red" },
  { eventFilter: throttleFilter(1000) }
);
</script>

<template>
  <h1 class="text-3xl font-bold underline text-emerald-600">Hello world!</h1>
  <div>x: {{ x }}</div>
  <div>y: {{ y }}</div>
</template>

<style lang="pcss"></style>
