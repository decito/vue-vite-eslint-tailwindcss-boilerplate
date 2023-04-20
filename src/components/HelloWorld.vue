<script setup lang="ts">
defineProps<{ msg: string }>()
</script>

<template>
  <div class="text-center lg:text-left">
    <h1 class="green -top-[10px] text-[2.6rem] font-medium">{{ msg }}</h1>
    <h3 class="text-xl">
      You've successfully created a project with
      <a href="https://vitejs.dev/" target="_blank" rel="noopener">Vite</a> +
      <a href="https://vuejs.org/" target="_blank" rel="noopener">Vue 3</a>.
      What's next?
    </h3>
  </div>
</template>
