<script setup lang="ts">
  import {useMouse} from '@vueuse/core'

  const {x, y} = useMouse()
</script>

<template>
  <h1 class="text-3xl font-bold underline text-emerald-600">Hello world!</h1>
  <div>x: {{ x }}</div>
  <div>y: {{ y }}</div>
</template>

<style lang="pcss"></style>
